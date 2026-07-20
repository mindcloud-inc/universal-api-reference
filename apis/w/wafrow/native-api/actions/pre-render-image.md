# Pre-render Image with Wafrow

Creates a pre-rendered image or PDF in Wafrow.

## Endpoint

- **Method:** `POST`
- **Path:** `/img/:template_id`
- **Base URL:** `https://wafrow.com/api`
- **Official documentation:** [Pre-render Image](https://wafrow.com/docs/api#/operations/imageMagic.createImage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | The Wafrow template UUID to pre-render immediately. |
| `personalize` | body | `object` | no | Layer overrides keyed by template layer name. |
