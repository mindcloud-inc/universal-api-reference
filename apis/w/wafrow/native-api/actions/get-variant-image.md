# Get Variant Image with Wafrow

Retrieves a rendered variant image from Wafrow.

## Endpoint

- **Method:** `GET`
- **Path:** `/i/:template_id/:campaign_id`
- **Base URL:** `https://wafrow.com/api`
- **Official documentation:** [Get Variant Image](https://wafrow.com/docs/api#/operations/imageMagic.serveVariant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | The Wafrow template UUID to render from the saved variant. |
| `campaign_id` | path | `string` | yes | The saved Wafrow campaign preset UUID returned by Save Variant. |
