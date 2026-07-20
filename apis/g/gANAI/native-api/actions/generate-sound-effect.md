# Generate Sound Effect with GAN.AI

Creates generated sound effects in GAN.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sfx/generate`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [Generate Sound Effect](https://developer.gan.ai/api-reference/sound-effects/generate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `creativity` | body | `number` | no |
| `duration_seconds` | body | `number` | no |
| `num_variations` | body | `number` | no |
| `prompt` | body | `string` | yes |
