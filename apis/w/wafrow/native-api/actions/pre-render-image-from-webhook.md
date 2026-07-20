# Pre-render Image From Webhook with Wafrow

Creates a pre-rendered image or PDF in Wafrow from webhook input.

## Endpoint

- **Method:** `POST`
- **Path:** `/i/:template_id`
- **Base URL:** `https://wafrow.com/api`
- **Official documentation:** [Pre-render Image From Webhook](https://wafrow.com/docs/api#/operations/imageMagic.generateFromWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | The Wafrow template UUID to pre-render from an inbound webhook payload. |
| `personalize` | body | `object` | no | Layer overrides keyed by template layer name. |
