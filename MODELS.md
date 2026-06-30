# Higgsfield CLI Models

Generated from `higgsfield model list` and `higgsfield model get <job_set_type>`. Run those commands for the live schema.

Required flags are listed per model below. Media inputs (`--image`, `--image-references`, `--start-image`, `--end-image`, `--video`, `--video-references`, `--audio`, `--audio-references`) accept either a UUID (upload id or previous job id) or a local file path; paths are auto-uploaded.


## Image (22)

### cinematic_studio_2_5 — Cinematic Studio 2.5

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k`, `4k` |

### flux_2 — FLUX.2

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image` (1+) | false | — | UUID or path |
| `--model` | false | `pro` | `pro`, `flex`, `max` |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k` |

### flux_kontext — Flux Kontext

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |

### gpt_image_2 — GPT Image 2

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16`, `3:2`, `2:3` |
| `--batch_size` | false | `1` | integer |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--quality` | false | `low` | `low`, `medium`, `high` |
| `--resolution` | false | `1k` | `1k`, `2k`, `4k` |

### grok_image — Grok Image

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image` (1+) | false | — | UUID or path |
| `--mode` | false | `std` | `std`, `pro` |
| `--prompt` | true | — | string |

### image_auto — Image Auto

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |

### image_background_remover — Image Background Remover

| flag | required | default | values |
|---|---|---|---|
| `--image` (single) | true | — | UUID or path |

Example:

```bash
higgsfield generate create image_background_remover --image ./image.png --wait
```

### kling_omni_image — Kling O1 Image

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `auto`, `16:9`, `9:16`, `4:3`, `3:4`, `3:2`, `2:3`, `21:9` |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k` |

### dtc_ads — DTC Ads Engine

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `auto`, `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `9:16`, `16:9`, `21:9`, `27:16`, `16:27`, `9:8`, `8:9`, `4:9`, `9:4` |
| `--batch_size` | false | `1` | integer (1..20) |
| `--brand_kit_id` | false | — | brand kit UUID |
| `--folder_id` | false | — | folder UUID |
| `--prompt` | true | — | string |
| `--quality` | false | `low` | `low`, `medium`, `high` |
| `--resolution` | false | `1k` | `1k`, `2k`, `4k` |
| `--style_id` | true | — | ad format UUID (from `marketing-studio ad-formats list`) |

### marketing_studio_image — Marketing Studio Image

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `auto`, `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `4:5`, `5:4`, `9:16`, `16:9`, `21:9` |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k`, `4k` |

### nano_banana — Nano Banana

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `auto`, `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `4:5`, `5:4`, `9:16`, `16:9`, `21:9` |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |

### nano_banana_2 — Nano Banana Pro

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `4:5`, `5:4`, `9:16`, `16:9`, `21:9` |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k`, `4k` |

### nano_banana_2_lite — Nano Banana 2 Lite

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | string |
| `--image-references` (or `--image`) (0..14) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | string |

Constraints:

- A non-empty prompt or at least one image reference is required.
- At most 14 image references are allowed.
- `--aspect_ratio auto` requires at least one image reference.

Example:

```bash
higgsfield generate create nano_banana_2_lite --prompt "clean product sketch, white background" --image ./reference.png --resolution 1k --wait
```

### nano_banana_flash — Nano Banana 2

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `4:5`, `5:4`, `9:16`, `16:9`, `21:9` |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k`, `4k` |

### openai_hazel — OpenAI Hazel

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--quality` | false | `medium` | `low`, `medium`, `high` |

### outpaint — Outpaint

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `21:9` | `auto`, `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `4:5`, `5:4`, `9:16`, `16:9`, `21:9` |
| `--image` (single) | true | — | UUID or path |

Example:

```bash
higgsfield generate create outpaint --image ./image.png --aspect_ratio 16:9 --wait
```

### recraft_v4_1 — Recraft V4.1

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `3:4`, `4:3`, `4:5`, `5:4`, `3:2`, `2:3`, `16:9`, `9:16`, `21:9` |
| `--background_color` | false | — | string |
| `--batch_size` | false | `1` | integer (1..4) |
| `--colors` | false | — | array |
| `--model_type` | false | `standard` | `standard`, `vector`, `utility`, `utility_vector` |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k` |

Example:

```bash
higgsfield generate create recraft_v4_1 --prompt "minimal vector logo mark for a coffee brand" --model_type vector --resolution 2k --wait
```

### seedream_v4_5 — Seedream 4.5

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `16:9`, `3:2`, `21:9`, `3:4`, `9:16`, `2:3` |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--quality` | false | `basic` | `basic`, `high` |

### seedream_v5_lite — Seedream V5 Lite

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--quality` | false | `basic` | `basic`, `high` |

### soul_cinematic — Soul Cinematic

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |

### soul_location — Soul Location

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--prompt` | true | — | string |

### text2image_soul_v2 — Higgsfield Soul V2

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--soul-id` | false | — | Soul UUID |
| `--image` (1+) | false | — | UUID or path |
| `--prompt` | true | — | string |

### z_image — Z Image

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--prompt` | true | — | string |

## Video (21)

### brain_activity — Virality Predictor

| flag | required | default | values |
|---|---|---|---|
| `--video` (single) | true | — | UUID or path |

### cinematic_studio_3_0 — Cinematic Studio 3.0

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1` |
| `--duration` | false | `5` | integer |
| `--start-image`, `--end-image`, `--image`, `--video`, `--audio` | false | — | UUID or path |
| `--prompt` | true | — | string |

### cinematic_studio_video — Cinematic Studio Video

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--duration` | false | `5` | `5`, `10` |
| `--start-image`, `--end-image`, `--image`, `--video`, `--audio` | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--slow_motion` | false | `false` | boolean |
| `--sound` | false | `true` | boolean |

### cinematic_studio_video_v2 — Cinematic Studio Video V2

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--duration` | false | `5` | integer |
| `--genre` | false | `auto` | `auto`, `action`, `horror`, `comedy`, `western`, `suspense`, `intimate`, `spectacle` |
| `--start-image`, `--end-image`, `--image`, `--video`, `--audio` | false | — | UUID or path |
| `--mode` | false | `std` | `pro`, `std` |
| `--prompt` | true | — | string |

### grok_video — Grok Video

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1` |
| `--duration` | false | `5` | integer |
| `--start-image`, `--end-image`, `--image`, `--video`, `--audio` | false | — | UUID or path |
| `--prompt` | true | — | string |

### grok_video_v15 — Grok Video 1.5

| flag | required | default | values |
|---|---|---|---|
| `--duration` | false | `5` | integer (2..15) |
| one of `--start-image`, `--image` | true | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `480p`, `720p` |

Example:

```bash
higgsfield generate create grok_video_v15 --prompt "cinematic handheld shot, neon rainy street" --start-image ./image.png --duration 5 --resolution 720p --wait
```

### gemini_omni — Gemini Omni Flash

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | string |
| `--duration` | false | `8` | integer |
| `--image-references` (or `--image`) (0..7) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | string |
| `--video-references` (or `--video`) (0..1) | false | — | UUID or path |

Constraints:

- At most 1 video reference is allowed.
- When a video reference is provided, at most 5 image references are allowed.
- At most 7 image references are allowed.

Example:

```bash
higgsfield generate create gemini_omni --prompt "cinematic product reveal with smooth camera motion" --image ./product.png --duration 8 --resolution 720p --wait
```

### kling2_6 — Kling 2.6 Video

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1` |
| `--duration` | false | `5` | `5`, `10` |
| `--image` (single) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--sound` | false | `true` | boolean |

### kling3_0 — Kling v3.0

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1` |
| `--duration` | false | `5` | integer |
| `--start-image`, `--end-image`, `--image`, `--video`, `--audio` | false | — | UUID or path |
| `--mode` | false | `std` | `pro`, `std` |
| `--prompt` | true | — | string |
| `--sound` | false | `on` | `on`, `off` |

### kling3_0_turbo — Kling 3.0 Turbo

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1` |
| `--duration` | false | `5` | integer (3..15) |
| one of `--start-image` | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `720p`, `1080p` |

Example:

```bash
higgsfield generate create kling3_0_turbo --prompt "fast handheld product reveal on a clean studio table" --start-image ./first.png --duration 5 --resolution 720p --wait
```

### marketing_studio_video — Marketing Studio Video

| flag | required | default | values |
|---|---|---|---|
| `--ad_reference_id` | false | — | object (ad-reference UUID) |
| `--aspect_ratio` | false | `16:9` | `auto`, `21:9`, `16:9`, `4:3`, `1:1`, `3:4`, `9:16` |
| `--avatars` | false | — | array |
| `--duration` | false | `15` | integer |
| `--generate_audio` | false | `false` | boolean |
| `--hook_id` | false | — | object (hook UUID) |
| `--start-image`, `--end-image`, `--image`, `--video`, `--audio` | false | — | UUID or path |
| `--mode` | false | `ugc` | `ugc`, `ugc_how_to`, `ugc_unboxing`, `product_showcase`, `product_review`, `tv_spot`, `wild_card`, `ugc_virtual_try_on`, `virtual_try_on` |
| `--product_ids` | false | — | array |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `480p`, `720p`, `1080p` |
| `--setting_id` | false | — | object (setting UUID) |
| `--web_product_ids` | false | — | array |

### minimax_hailuo — Minimax Hailuo

| flag | required | default | values |
|---|---|---|---|
| `--duration` | false | `6` | `6`, `10` |
| `--image` (1+) | false | — | UUID or path |
| `--model` | false | `minimax-2.3` | `minimax`, `minimax-fast`, `minimax-2.3`, `minimax-2.3-fast` |
| `--prompt` | true | — | string |
| `--resolution` | false | `768` | `512`, `768`, `1080` |

### seedance1_5 — Seedance 1.5 Pro

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `auto`, `16:9`, `9:16`, `4:3`, `3:4`, `1:1`, `21:9` |
| `--duration` | false | `4` | `4`, `8`, `12` |
| `--start-image`, `--end-image`, `--image`, `--video`, `--audio` | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `480p`, `720p`, `1080p` |

### seedance_2_0 — Seedance 2.0

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `auto`, `16:9`, `9:16`, `4:3`, `3:4`, `1:1`, `21:9` |
| `--bitrate_mode` | false | `standard` | `standard`, `high` |
| `--duration` | false | `5` | integer |
| `--genre` | false | `auto` | `auto`, `action`, `horror`, `comedy`, `noir`, `drama`, `epic` |
| `--start-image`, `--end-image`, `--image`, `--video`, `--audio` | false | — | UUID or path |
| `--mode` | false | `std` | `std`, `fast` |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `480p`, `720p`, `1080p`, `4k` |

### soul_cast — Soul Cast

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--budget` | false | `50` | integer |
| `--prompt` | false | — | object |

### video_background_remover — Video Background Remover

| flag | required | default | values |
|---|---|---|---|
| `--video` (single) | true | — | UUID or path |

Example:

```bash
higgsfield generate create video_background_remover --video ./video.mp4 --wait
```

### veo3 — Google Veo 3

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16` |
| `--image` (single) | true | — | UUID or path |
| `--model` | false | `veo-3-fast` | `veo-3-preview`, `veo-3-fast` |
| `--prompt` | true | — | string |

### veo3_1 — Google Veo 3.1

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16` |
| `--duration` | false | `8` | `4`, `6`, `8` |
| `--image` (single) | false | — | UUID or path |
| `--model` | false | `veo-3-1-fast` | `veo-3-1-preview`, `veo-3-1-fast` |
| `--prompt` | true | — | string |
| `--quality` | false | `basic` | `basic`, `high`, `ultra` |

### veo3_1_lite — Google Veo 3.1 Lite

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `auto` |
| `--duration` | false | `8` | `4`, `6`, `8` |
| `--start-image`, `--end-image`, `--image`, `--video`, `--audio` | false | — | UUID or path |
| `--prompt` | true | — | string |

### wan2_6 — Wan 2.6 Video

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1` |
| `--duration` | false | `5` | `5`, `10`, `15` |
| `--start-image`, `--end-image`, `--image`, `--video`, `--audio` | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--quality` | false | `720p` | `720p`, `1080p` |

### wan2_7 — Wan 2.7

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1`, `4:3`, `3:4` |
| `--duration` | false | `5` | integer |
| `--start-image`, `--end-image`, `--image`, `--video`, `--audio` | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `720p`, `1080p` |

## 3D (1)

### multi_image_to_3d — Multi-Image to 3D

| flag | required | default | values |
|---|---|---|---|
| `--animation_action_id` | false | — | integer |
| `--enable_animation` | false | `false` | boolean |
| `--enable_pbr` | false | — | boolean |
| `--enable_rigging` | false | `false` | boolean |
| `--enable_safety_checker` | false | — | boolean |
| `--folder_id` | false | — | UUID |
| `--image` (1..4) | true | — | UUID or path |
| `--pose_mode` | false | — | string |
| `--rigging_height_meters` | false | — | number |
| `--seed` | false | — | integer |
| `--should_remesh` | false | — | boolean |
| `--should_texture` | false | `false` | boolean |
| `--symmetry_mode` | false | — | string |
| `--target_polycount` | false | — | integer |
| `--texture_image_url` | false | — | string |
| `--texture_prompt` | false | — | string |
| `--topology` | false | — | string |

Example:

```bash
higgsfield generate create multi_image_to_3d --image ./front.png --image ./side.png --should_texture true --wait
```

## Audio (3)

### sonilo_music — Sonilo Music

| flag | required | default | values |
|---|---|---|---|
| `--duration` | true | — | number |
| `--prompt` | true | — | string |

Example:

```bash
higgsfield generate create sonilo_music --prompt "cinematic synthwave track" --duration 12 --wait
```

### mirelo_text_to_audio — Mirelo Text to Audio

| flag | required | default | values |
|---|---|---|---|
| `--prompt` | true | — | string |

Example:

```bash
higgsfield generate create mirelo_text_to_audio --prompt "glass breaking in a large hall" --duration 4 --wait
```

### text2speech_v2 — Text to Speech

| flag | required | default | values |
|---|---|---|---|
| `--model` | true | — | `elevenlabs`, `minimax`, `seed_speech`, `vibe_voice`, `cozy_voice` |
| `--prompt` | true | — | string |
| `--voice_id` | true | — | string |
| `--voice_type` | true | — | `preset`, `element` |

Discover voices (`--voice_id` / `--voice_type`) with `higgsfield voices list`.

Example:

```bash
higgsfield generate create text2speech_v2 --prompt "Hello from Higgsfield" --model elevenlabs --voice_type preset --voice_id <voice_id> --wait
```
