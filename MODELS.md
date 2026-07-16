# Higgsfield CLI Models

Generated from `higgsfield model list` and `higgsfield model get <job_set_type>`. Run those commands for the live schema.

Required flags are listed per model below. Media inputs (`--image`, `--image-references`, `--start-image`, `--end-image`, `--video`, `--video-references`, `--audio`, `--audio-references`) accept either a UUID (upload id or previous job id) or a local file path; paths are auto-uploaded.

Every flag accepts both spellings: `--aspect_ratio` and `--aspect-ratio` are equivalent.


## Image (23)

### cinematic_studio_2_5 — Cinematic Studio 2.5

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `4:5`, `5:4`, `16:9`, `9:16`, `21:9` |
| `--batch_size` | false | `1` | integer |
| `--folder_id` | false | — | string |
| `--image-references` (or `--image`) (0..14) | false | — | UUID or path |
| `--mode` | false | `auto` | string |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k`, `4k` |

Constraints:

- At most 14 image references are allowed.

### flux_2 — FLUX.2

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k` |
| `--variant` | false | `pro` | `pro`, `flex`, `max` |

### flux_kontext — Flux Kontext

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image-references` (or `--image`) (0..4) | false | — | UUID or path |
| `--prompt` | true | — | string |

Constraints:

- At most 4 image_references are allowed.

### gpt_image_2 — GPT Image 2

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16`, `3:2`, `2:3` |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--quality` | false | `high` | `low`, `medium`, `high` |
| `--resolution` | false | `2k` | `1k`, `2k`, `4k` |

### grok_image — Grok Image

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `auto`, `1:2`, `2:1`, `3:2`, `2:3`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--mode` | false | `std` | `std`, `quality` |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k` |

### image_auto — Image Auto

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image-references` (or `--image`) (0..14) | false | — | UUID or path |
| `--prompt` | true | — | string |

Constraints:

- At most 14 image references are allowed.

### image_background_remover — Image Background Remover

| flag | required | default | values |
|---|---|---|---|
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |

Constraints:

- Exactly one image_references entry is required.

Example:

```bash
higgsfield generate create image_background_remover --image ./image.png --wait
```

### kling_omni_image — Kling O1 Image

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `auto`, `16:9`, `9:16`, `4:3`, `3:4`, `3:2`, `2:3`, `21:9` |
| `--image-references` (or `--image`) (0..10) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k` |

Constraints:

- At most 10 image_references are allowed.
- Aspect_ratio 'auto' requires at least one image_reference.

### marketing_studio_image — Marketing Studio Image

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `auto`, `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `4:5`, `5:4`, `9:16`, `16:9`, `21:9` |
| `--image-references` (or `--image`) (0..14) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k`, `4k` |

Constraints:

- At most 14 image_references are allowed.
- Aspect_ratio 'auto' requires at least one image_reference.
- 'prompt' or at least one image_reference is required.

### nano_banana — Nano Banana

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `4:5`, `5:4`, `9:16`, `16:9`, `21:9` |
| `--image-references` (or `--image`) (0..8) | false | — | UUID or path |
| `--prompt` | true | — | string |

Constraints:

- At most 8 image_references are allowed.

### nano_banana_2 — Nano Banana Pro

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `4:5`, `5:4`, `9:16`, `16:9`, `21:9` |
| `--image-references` (or `--image`) (0..14) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `2k` | `1k`, `2k`, `4k` |

Constraints:

- A non-empty prompt or at least one image reference is required.
- At most 14 image references are allowed.

### nano_banana_2_lite — Nano Banana 2 Lite

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `auto`, `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `4:5`, `5:4`, `9:16`, `16:9`, `21:9` |
| `--image-references` (or `--image`) (0..14) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k` |
| `--thinking` | false | `HIGH` | `MINIMAL`, `HIGH` |

Constraints:

- A non-empty prompt or at least one image reference is required.
- At most 14 image references are allowed.
- Aspect_ratio 'auto' requires at least one image reference.

Example:

```bash
higgsfield generate create nano_banana_2_lite --prompt "clean product sketch, white background" --image ./reference.png --resolution 1k --wait
```

### nano_banana_flash — Nano Banana 2

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `4:5`, `5:4`, `9:16`, `16:9`, `21:9` |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k`, `4k` |

### openai_hazel — OpenAI Hazel

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `3:2`, `2:3`, `auto` |
| `--image-references` (or `--image`) (0..16) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--quality` | false | `medium` | `low`, `medium`, `high` |

Constraints:

- Aspect_ratio 'auto' requires at least one image reference.
- At most 16 image references are allowed.

### outpaint — Outpaint

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `21:9` | `auto`, `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `4:5`, `5:4`, `9:16`, `16:9`, `21:9` |
| `--folder_id` | false | — | string |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |

Constraints:

- Exactly one image_references entry is required.

Example:

```bash
higgsfield generate create outpaint --image ./image.png --aspect_ratio 16:9 --wait
```

### recraft_v4_1 — Recraft V4.1

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `3:4`, `4:3`, `4:5`, `5:4`, `3:2`, `2:3`, `16:9`, `9:16` |
| `--background_color` | false | — | string |
| `--colors` | false | — | array |
| `--model_type` | false | `standard` | `standard`, `vector`, `utility`, `utility_vector` |
| `--prompt` | true | — | string |
| `--resolution` | false | `1k` | `1k`, `2k` |

Constraints:

- Each color in colors must be a #RRGGBB hex string (six hex digits, no alpha).
- Background_color must be a #RRGGBB hex string (six hex digits, no alpha) or null.

Example:

```bash
higgsfield generate create recraft_v4_1 --prompt "minimal vector logo mark for a coffee brand" --model_type vector --resolution 2k --wait
```

### seedream_v4_5 — Seedream 4.5

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `16:9`, `3:2`, `21:9`, `3:4`, `9:16`, `2:3` |
| `--image-references` (or `--image`) (0..14) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--quality` | false | `basic` | `basic`, `high` |

Constraints:

- At most 14 image_references are allowed.

### seedream_v5_lite — Seedream V5 Lite

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--quality` | false | `basic` | `basic`, `high` |

### soul_cast — Soul Cast

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | true | — | `16:9` |
| `--budget` | false | `50` | integer |
| `--prompt` | false | — | string |

### soul_cinematic — Soul Cinematic

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `16:9`, `9:16`, `4:3`, `3:4`, `3:2`, `2:3`, `21:9` |
| `--image-references` (or `--image`) (single) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--quality` | false | `2k` | `1.5k`, `2k` |
| `--soul-id` (or `--custom-reference-id`) | false | — | Soul UUID |

Constraints:

- At most one image reference is allowed.

### soul_location — Soul Location

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `16:9`, `9:16`, `4:3`, `3:4`, `3:2`, `2:3`, `21:9`, `9:21` |
| `--prompt` | true | — | string |

### text2image_soul_v2 — Higgsfield Soul V2

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `16:9`, `9:16`, `4:3`, `3:4`, `3:2`, `2:3` |
| `--image-references` (or `--image`) (single) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--quality` | false | `2k` | `1.5k`, `2k` |
| `--soul-id` (or `--custom-reference-id`) | false | — | Soul UUID |

Constraints:

- At most one image reference is allowed.

### z_image — Z Image

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `1:1` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--prompt` | true | — | string |

## Video (22)

### brain_activity — Virality Predictor

| flag | required | default | values |
|---|---|---|---|
| `--folder_id` | false | — | string |
| `--video` (single) | true | — | UUID or path |

Analyzes a video and predicts audience engagement. Pass the video with `--video`.

### cinematic_studio_3_0 — Cinematic Studio 3.0

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `auto`, `21:9`, `16:9`, `4:3`, `1:1`, `3:4`, `9:16` |
| `--audio-references` (or `--audio`) (repeated) | false | — | UUID or path |
| `--batch_size` | false | `1` | integer |
| `--duration` | false | `5` | integer |
| `--end-image` (single) | false | — | UUID or path |
| `--enhance_prompt` | false | `false` | boolean |
| `--folder_id` | false | — | string |
| `--generate_audio` | false | `false` | boolean |
| `--genre` | false | `auto` | `auto`, `action`, `horror`, `comedy`, `noir`, `drama`, `epic` |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--multi_prompt` | false | — | array |
| `--multi_shot_mode` | false | `custom` | `auto`, `custom` |
| `--multi_shots` | false | `false` | boolean |
| `--preset_id` | false | — | string |
| `--prompt` | true | — | string |
| `--prompt_language` | false | `zh` | `en`, `zh` |
| `--resolution` | false | `720p` | `480p`, `720p`, `1080p`, `4k` |
| `--speedramp` | false | `auto` | `auto`, `linear`, `slowmo`, `speedup`, `fast_to_slowmo`, `slowmo_to_fast`, `super_slowmo`, `impact` |
| `--start-image` (single) | false | — | UUID or path |
| `--video-references` (or `--video`) (repeated) | false | — | UUID or path |

Constraints:

- At most 15 media references are allowed in total.

### cinematic_studio_video — Cinematic Studio Video

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--duration` | false | `5` | `5`, `10` |
| `--end-image` (single) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--slow_motion` | false | `false` | boolean |
| `--sound` | false | `true` | boolean |
| `--start-image` (single) | false | — | UUID or path |

Constraints:

- End_image requires start_image to also be provided.

### cinematic_studio_video_3_5 — Cinematic Studio Video 3.5

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `auto` | `auto`, `21:9`, `16:9`, `4:3`, `1:1`, `3:4`, `9:16` |
| `--audio-references` (or `--audio`) (0..15) | false | — | UUID or path |
| `--camera_style` | false | — | `classic_static`, `silent_machine`, `one_take`, `epic_scale`, `intimate_observer`, `impossible_camera`, `documentary_snap`, `raw_chaos`, `dreamy_flow` |
| `--color_grading` | false | — | `naturalistic_clean`, `bleached_warm`, `hyper_neon`, `teal_orange_epic`, `sodium_decay`, `cold_steel`, `bleach_bypass`, `classic_bw` |
| `--duration` | false | `15` | integer |
| `--end-image` (single) | false | — | UUID or path |
| `--enhance_prompt` | false | `false` | boolean |
| `--generate_audio` | false | `false` | boolean |
| `--genre` | false | `auto` | `auto`, `action`, `horror`, `comedy`, `noir`, `drama`, `epic` |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--light_scheme` | false | — | `soft_cross`, `contre_jour`, `overhead_fall`, `window`, `practicals`, `silhouette` |
| `--multi_prompt` | false | — | array |
| `--multi_shot_mode` | false | `custom` | `auto`, `custom` |
| `--multi_shots` | false | `false` | boolean |
| `--prompt` | false | — | string |
| `--prompt_language` | false | `zh` | `en`, `zh` |
| `--resolution` | false | `720p` | `480p`, `720p`, `1080p` |
| `--start-image` (single) | false | — | UUID or path |
| `--style_prompt` | false | — | string |
| `--video-references` (or `--video`) (repeated) | false | — | UUID or path |

Constraints:

- At most 15 media references are allowed in total (image_references + start_image + end_image + video_references + audio_references).
- Inline style axes (camera_style/light_scheme/color_grading) and style_prompt are mutually exclusive.

### cinematic_studio_video_v2 — Cinematic Studio Video V2

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `1:1`, `4:3`, `3:4`, `16:9`, `9:16` |
| `--batch_size` | false | `1` | integer |
| `--cfg_scale` | false | `0.5` | number |
| `--duration` | false | `5` | integer |
| `--end-image` (single) | false | — | UUID or path |
| `--folder_id` | false | — | string |
| `--genre` | false | `auto` | `auto`, `action`, `horror`, `comedy`, `western`, `suspense`, `intimate`, `spectacle` |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--kling_element_ids` | false | — | array |
| `--mode` | false | `std` | `pro`, `std` |
| `--multi_prompt` | false | — | array |
| `--multi_shot_mode` | false | `custom` | `auto`, `custom` |
| `--multi_shots` | false | `false` | boolean |
| `--preset_id` | false | — | string |
| `--prompt` | true | — | string |
| `--sound` | false | `on` | `on`, `off` |
| `--speedramp` | false | `auto` | `auto`, `custom`, `linear`, `slowmo`, `speedup`, `impact` |
| `--start-image` (single) | false | — | UUID or path |

### gemini_omni — Gemini Omni Flash

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16` |
| `--duration` | false | `8` | `4`, `6`, `8`, `10` |
| `--image-references` (or `--image`) (0..7) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `720p` |
| `--video-references` (or `--video`) (single) | false | — | UUID or path |

Constraints:

- At most 1 video_references entry is allowed.
- When a video reference is provided, at most 5 image_references are allowed.
- At most 7 image_references are allowed.

Example:

```bash
higgsfield generate create gemini_omni --prompt "cinematic product reveal with smooth camera motion" --image ./product.png --duration 8 --resolution 720p --wait
```

### grok_video — Grok Video

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1` |
| `--duration` | false | `5` | integer |
| `--prompt` | true | — | string |
| `--start-image` (single) | false | — | UUID or path |

### grok_video_v15 — Grok Video 1.5

| flag | required | default | values |
|---|---|---|---|
| `--duration` | false | `5` | integer |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `480p`, `720p` |
| `--start-image` (single) | true | — | UUID or path |

Example:

```bash
higgsfield generate create grok_video_v15 --prompt "cinematic handheld shot, neon rainy street" --start-image ./image.png --duration 5 --resolution 720p --wait
```

### kling2_6 — Kling 2.6 Video

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1` |
| `--duration` | false | `5` | `5`, `10` |
| `--prompt` | true | — | string |
| `--sound` | false | `true` | boolean |
| `--start-image` (single) | false | — | UUID or path |

### kling3_0 — Kling v3.0

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1` |
| `--duration` | false | `5` | integer |
| `--end-image` (single) | false | — | UUID or path |
| `--mode` | false | `std` | `std`, `pro`, `4k` |
| `--prompt` | true | — | string |
| `--sound` | false | `on` | `on`, `off` |
| `--start-image` (single) | false | — | UUID or path |

### kling3_0_turbo — Kling 3.0 Turbo

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1` |
| `--duration` | false | `5` | integer |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `720p`, `1080p` |
| `--start-image` (single) | false | — | UUID or path |

Example:

```bash
higgsfield generate create kling3_0_turbo --prompt "fast handheld product reveal on a clean studio table" --start-image ./first.png --duration 5 --resolution 720p --wait
```

### marketing_studio_video — Marketing Studio Video

| flag | required | default | values |
|---|---|---|---|
| `--ad_reference_id` | false | — | ad-reference UUID |
| `--aspect_ratio` | false | `16:9` | `auto`, `21:9`, `16:9`, `4:3`, `1:1`, `3:4`, `9:16` |
| `--avatar_ids` | false | — | array |
| `--avatars` | false | — | array |
| `--duration` | false | `15` | integer |
| `--end-image` (single) | false | — | UUID or path |
| `--generate_audio` | false | `false` | boolean |
| `--hook_id` | false | — | hook UUID |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--mode` | false | `ugc` | string |
| `--product_ids` | false | — | array |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `480p`, `720p`, `1080p` |
| `--setting_id` | false | — | setting UUID |
| `--specific_mode` | false | `default` | `default`, `web_product`, `from_storyboard` |
| `--start-image` (single) | false | — | UUID or path |
| `--storyboard_id` | false | — | storyboard UUID |
| `--web_product_ids` | false | — | array |
| `--web_product_type` | false | — | `desktop`, `mobile` |

Constraints:

- Ad_reference_id cannot be combined with hook_id or setting_id.
- Product_ids and web_product_ids cannot both be set.

### minimax_hailuo — Minimax Hailuo

| flag | required | default | values |
|---|---|---|---|
| `--duration` | false | `6` | `6`, `10` |
| `--end-image` (single) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `768` | `512`, `768`, `1080` |
| `--start-image` (single) | false | — | UUID or path |
| `--variant` | false | `minimax-2.3` | `minimax`, `minimax-fast`, `minimax-2.3`, `minimax-2.3-fast` |

Constraints:

- Resolution '512' is incompatible with end_image.
- Resolution '512' is not supported for 'minimax-2.3' or 'minimax-2.3-fast'.
- Resolution '1080' is not available for 10 second duration.
- Start_image or end_image is required unless variant is 'minimax-2.3'.
- End_image is not supported for 'minimax-2.3' or 'minimax-2.3-fast'.

### seedance1_5 — Seedance 1.5 Pro

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `auto`, `16:9`, `9:16`, `4:3`, `3:4`, `1:1`, `21:9` |
| `--duration` | false | `4` | `4`, `8`, `12` |
| `--end-image` (single) | false | — | UUID or path |
| `--generate_audio` | false | `true` | boolean |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `480p`, `720p`, `1080p` |
| `--start-image` (single) | false | — | UUID or path |

Constraints:

- End_image requires start_image to be set.

### seedance_2_0 — Seedance 2.0

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `auto`, `16:9`, `9:16`, `4:3`, `3:4`, `1:1`, `21:9` |
| `--audio-references` (or `--audio`) (0..3) | false | — | UUID or path |
| `--bitrate_mode` | false | `standard` | `standard`, `high` |
| `--duration` | false | `5` | integer |
| `--end-image` (single) | false | — | UUID or path |
| `--generate_audio` | false | `true` | boolean |
| `--genre` | false | `auto` | `auto`, `action`, `horror`, `comedy`, `noir`, `drama`, `epic` |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--mode` | false | `std` | `std`, `fast` |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `480p`, `720p`, `1080p`, `4k` |
| `--start-image` (single) | false | — | UUID or path |
| `--video-references` (or `--video`) (0..3) | false | — | UUID or path |

Constraints:

- At most 9 image references are allowed (counting start_image and end_image).
- At most 3 video_references are allowed.
- At most 3 audio_references are allowed.
- At most 12 reference files are allowed in total across images, videos, and audios (including start_image and end_image).
- Audio_references require at least one image, video, start_image, or end_image.
- Mode 'fast' supports only 480p/720p; use mode 'std' for 1080p/4k.

### seedance_2_0_mini — Seedance 2.0 Mini

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `auto`, `16:9`, `9:16`, `4:3`, `3:4`, `1:1`, `21:9` |
| `--audio-references` (or `--audio`) (0..3) | false | — | UUID or path |
| `--bitrate_mode` | false | `standard` | `standard`, `high` |
| `--duration` | false | `5` | integer |
| `--end-image` (single) | false | — | UUID or path |
| `--generate_audio` | false | `true` | boolean |
| `--genre` | false | `auto` | `auto`, `action`, `horror`, `comedy`, `noir`, `drama`, `epic` |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `480p`, `720p` |
| `--start-image` (single) | false | — | UUID or path |
| `--video-references` (or `--video`) (0..3) | false | — | UUID or path |

Constraints:

- At most 9 image references are allowed (counting start_image and end_image).
- At most 3 video_references are allowed.
- At most 3 audio_references are allowed.
- At most 12 reference files are allowed in total across images, videos, and audios (including start_image and end_image).
- Audio_references require at least one image, video, start_image, or end_image.

### veo3 — Google Veo 3

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16` |
| `--prompt` | true | — | string |
| `--start-image` (single) | true | — | UUID or path |
| `--variant` | false | `veo-3-fast` | `veo-3-preview`, `veo-3-fast` |

### veo3_1 — Google Veo 3.1

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16` |
| `--duration` | false | `8` | `4`, `6`, `8` |
| `--prompt` | true | — | string |
| `--quality` | false | `basic` | `basic`, `high`, `ultra` |
| `--start-image` (single) | false | — | UUID or path |
| `--variant` | false | `veo-3-1-fast` | `veo-3-1-preview`, `veo-3-1-fast` |

### veo3_1_lite — Google Veo 3.1 Lite

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `auto` |
| `--duration` | false | `8` | `4`, `6`, `8` |
| `--end-image` (single) | false | — | UUID or path |
| `--generate_audio` | false | `false` | boolean |
| `--prompt` | true | — | string |
| `--start-image` (single) | false | — | UUID or path |

Constraints:

- Duration must be 8 when both start_image and end_image are set.

### video_background_remover — Video Background Remover

| flag | required | default | values |
|---|---|---|---|
| `--video-references` (or `--video`) (repeated) | false | — | UUID or path |

Constraints:

- Exactly one video is required in video_references.

Example:

```bash
higgsfield generate create video_background_remover --video ./video.mp4 --wait
```

### wan2_6 — Wan 2.6 Video

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1` |
| `--audio-references` (or `--audio`) (repeated) | false | — | UUID or path |
| `--duration` | false | `5` | `5`, `10`, `15` |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--quality` | false | `720p` | `720p`, `1080p` |
| `--video-references` (or `--video`) (repeated) | false | — | UUID or path |

Constraints:

- Reference-to-video (with video_references) supports only 5 or 10 second durations.

### wan2_7 — Wan 2.7

| flag | required | default | values |
|---|---|---|---|
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16`, `1:1`, `4:3`, `3:4` |
| `--audio-references` (or `--audio`) (single) | false | — | UUID or path |
| `--duration` | false | `5` | integer |
| `--end-image` (single) | false | — | UUID or path |
| `--prompt` | true | — | string |
| `--resolution` | false | `720p` | `720p`, `1080p` |
| `--start-image` (single) | false | — | UUID or path |

Constraints:

- End_image requires start_image.
- At most 1 audio reference is allowed.

## Video explainer jobs

These job types have similar names but different responsibilities:

- `explainer_video` assembles ordered video/audio block pairs and is the final step used by the public explainer skill.
- `video_explainer` is an alternate monolithic server-run workflow. The public skill does not use it.

### video_explainer — Explainer Video

| flag | required | default | values |
|---|---|---|---|
| `--prompt` | conditional | — | string, max 5000 characters |
| `--medias` | false | `[]` | JSON array via `@file`; up to 14 images/files |
| `--aspect_ratio` | false | `16:9` | `16:9`, `9:16` |
| `--duration` | true | — | integer, 20–600, multiple of 10 |
| `--preset_id` | false | — | UUID from `higgsfield preset list video-explainer` |
| `--voice_type` | false | — | `preset`, `element` |
| `--voice_id` | false | — | voice ID from `higgsfield voices list` |
| `--folder_id` | false | — | UUID |

Constraints:

- `prompt` is required unless at least one image/file is attached.
- Video and audio attachments are rejected.
- `voice_type` and `voice_id` must be provided together.
- `preset_id` controls style only; it does not replace the topic.
- Job creation resolves the preset and imports its hidden style image automatically.

Examples:

```bash
higgsfield preset list video-explainer --json

higgsfield generate create video_explainer \
  --prompt "Explain compound interest to teenagers. Narration language: English." \
  --duration 60 \
  --aspect_ratio 16:9 \
  --preset_id <preset_id> \
  --wait

higgsfield generate create video_explainer \
  --prompt "Explain the supplied diagrams. Narration language: Spanish." \
  --image ./diagram-1.png \
  --image ./diagram-2.png \
  --duration 90 \
  --aspect_ratio 9:16 \
  --voice_type preset \
  --voice_id <voice_id> \
  --wait
```

This job remains available as a direct API surface, but `higgsfield-video-explainer`
uses separately generated Seed Audio and Gemini Omni blocks followed by
`explainer_video` so every narration take maps explicitly to one clip.

### explainer_video — Explainer Video Assembler

Assembler for callers that already generated ordered clip/audio pairs. It does
not plan a narrative, choose a style, generate clips, or create narration.

| flag | required | default | values |
|---|---|---|---|
| `--width` | true | — | even integer greater than 1 |
| `--height` | true | — | even integer greater than 1 |
| `--items` | true | — | JSON array via `@file`; at least 2 items |
| `--subtitles` | false | — | JSON object; font: `patrick`, `caveat`, `marker`, `anton` |

Each item contains `video: {id,type}` and optional `audio: {id,type}`. Completed
generation jobs may use the generic types `video_job` and `audio_job`:

```json
[
  {
    "video": {"id": "<clip-1-job-id>", "type": "video_job"},
    "audio": {"id": "<voice-1-job-id>", "type": "audio_job"}
  },
  {
    "video": {"id": "<clip-2-job-id>", "type": "video_job"},
    "audio": {"id": "<voice-2-job-id>", "type": "audio_job"}
  }
]
```

```bash
higgsfield generate create explainer_video \
  --items @blocks.json \
  --width 1280 \
  --height 720 \
  --subtitles '{"font":"patrick"}' \
  --wait
```

## 3D (5)

### 3d_rigging — 3D Rigging

| flag | required | default | values |
|---|---|---|---|
| `--animation_action_id` | false | — | integer |
| `--enable_animation` | false | `false` | boolean |
| `--enable_safety_checker` | false | — | boolean |
| `--folder_id` | false | — | string |
| `--height_meters` | false | — | number |
| `--model_url` | true | — | string |

### image_to_3d — Image to 3D

| flag | required | default | values |
|---|---|---|---|
| `--animation_action_id` | false | — | integer |
| `--enable_animation` | false | `false` | boolean |
| `--enable_pbr` | false | — | boolean |
| `--enable_rigging` | false | `false` | boolean |
| `--enable_safety_checker` | false | — | boolean |
| `--folder_id` | false | — | string |
| `--image-references` (or `--image`) (repeated) | true | — | UUID or path |
| `--pose_mode` | false | — | `a-pose`, `t-pose` |
| `--rigging_height_meters` | false | — | number |
| `--seed` | false | — | integer |
| `--should_remesh` | false | — | boolean |
| `--should_texture` | false | `false` | boolean |
| `--symmetry_mode` | false | — | `off`, `auto`, `on` |
| `--target_polycount` | false | — | integer |
| `--texture_image_url` | false | — | string |
| `--texture_prompt` | false | — | string |
| `--topology` | false | — | `quad`, `triangle` |

Constraints:

- Enable_animation requires enable_rigging=true.
- Animation_action_id is required when enable_animation=true.
- Texture_prompt requires should_texture=true.
- Texture_image_url requires should_texture=true.
- Enable_pbr requires should_texture=true.

### multi_image_to_3d — Multi-Image to 3D

| flag | required | default | values |
|---|---|---|---|
| `--animation_action_id` | false | — | integer |
| `--enable_animation` | false | `false` | boolean |
| `--enable_pbr` | false | — | boolean |
| `--enable_rigging` | false | `false` | boolean |
| `--enable_safety_checker` | false | — | boolean |
| `--folder_id` | false | — | string |
| `--image-references` (or `--image`) (repeated) | true | — | UUID or path |
| `--pose_mode` | false | — | `a-pose`, `t-pose` |
| `--rigging_height_meters` | false | — | number |
| `--seed` | false | — | integer |
| `--should_remesh` | false | — | boolean |
| `--should_texture` | false | `false` | boolean |
| `--symmetry_mode` | false | — | `off`, `auto`, `on` |
| `--target_polycount` | false | — | integer |
| `--texture_image_url` | false | — | string |
| `--texture_prompt` | false | — | string |
| `--topology` | false | — | `quad`, `triangle` |

Constraints:

- Enable_animation requires enable_rigging=true.
- Animation_action_id is required when enable_animation=true.
- Texture_prompt requires should_texture=true.
- Texture_image_url requires should_texture=true.
- Enable_pbr requires should_texture=true.

Example:

```bash
higgsfield generate create multi_image_to_3d --image ./front.png --image ./side.png --should_texture true --wait
```

### sam_3_3d — 3D Objects

| flag | required | default | values |
|---|---|---|---|
| `--detection_threshold` | false | — | number |
| `--export_textured_glb` | false | `true` | boolean |
| `--folder_id` | false | — | string |
| `--image-references` (or `--image`) (repeated) | true | — | UUID or path |
| `--prompt` | false | — | string |
| `--seed` | false | — | integer |

### tripo_3d — Text to 3D

| flag | required | default | values |
|---|---|---|---|
| `--auto_size` | false | `false` | boolean |
| `--face_limit` | false | — | integer |
| `--geometry_quality` | false | `standard` | `standard`, `detailed` |
| `--negative_prompt` | false | — | string |
| `--pbr` | false | `true` | boolean |
| `--prompt` | true | — | string |
| `--texture` | false | `true` | boolean |
| `--texture_quality` | false | `standard` | `standard`, `detailed` |

## Audio (5)

### inworld_text_to_speech — Inworld Text to Speech

| flag | required | default | values |
|---|---|---|---|
| `--prompt` | true | — | string |
| `--voice` | true | — | 113 built-in voices — run `higgsfield model get inworld_text_to_speech` for the list |

### mirelo_text_to_audio — Mirelo Text to Audio

| flag | required | default | values |
|---|---|---|---|
| `--duration` | true | — | number |
| `--prompt` | true | — | string |

Example:

```bash
higgsfield generate create mirelo_text_to_audio --prompt "glass breaking in a large hall" --duration 4 --wait
```

### seed_audio — Seed Audio 1.0

| flag | required | default | values |
|---|---|---|---|
| `--audio-references` (or `--audio`) (0..2) | false | — | UUID or path |
| `--format` | false | `wav` | `wav`, `mp3`, `pcm`, `ogg_opus` |
| `--image-references` (or `--image`) (repeated) | false | — | UUID or path |
| `--loudness_rate` | false | `0` | integer |
| `--pitch_rate` | false | `0` | integer |
| `--prompt` | true | — | string |
| `--sample_rate` | false | `24000` | `8000`, `16000`, `24000`, `32000`, `44100`, `48000` |
| `--speech_rate` | false | `0` | integer |
| `--voice_id` | false | — | string |
| `--voice_type` | false | — | `preset`, `element` |

For a cloned or preset voice, take `--voice_id` and `--voice_type` from `higgsfield voices list`.

Constraints:

- Image_references and audio_references are mutually exclusive.
- Voice_type and voice_id must be provided together.
- A voice cannot be combined with an image reference.
- A voice allows at most 2 additional audio references.

Example:

```bash
higgsfield generate create seed_audio --prompt "Welcome to the show!" --voice_type preset --voice_id <voice_id> --wait
```

### sonilo_music — Sonilo Music

| flag | required | default | values |
|---|---|---|---|
| `--duration` | true | — | number |
| `--prompt` | true | — | string |

Example:

```bash
higgsfield generate create sonilo_music --prompt "cinematic synthwave track" --duration 12 --wait
```

### text2speech_v2 — Text to Speech

| flag | required | default | values |
|---|---|---|---|
| `--prompt` | true | — | string |
| `--variant` | true | — | `elevenlabs`, `minimax`, `seed_speech`, `vibe_voice`, `cozy_voice` |
| `--voice_id` | true | — | string |
| `--voice_type` | true | — | `preset`, `element` |

Discover voices (`--voice_id` / `--voice_type`) with `higgsfield voices list`.

Constraints:

- Prompt character limit depends on the engine: elevenlabs/vibe_voice/cozy_voice 5000, minimax 10000, seed_speech 15000.

Example:

```bash
higgsfield generate create text2speech_v2 --prompt "Hello from Higgsfield" --variant elevenlabs --voice_type preset --voice_id <voice_id> --wait
```

Additional utility job types (upscale, background removal, transcription, etc.) are available; run `higgsfield model get <job_type>` for their schemas: `autosprite`, `bytedance_image_upscale`, `bytedance_video_upscale`, `clipify`, `color_grading_lut`, `llm_text`, `sam_3_video`, `speech2text`, `topaz_image`, `topaz_video`, `video_deflicker`, `video_upscale`.
