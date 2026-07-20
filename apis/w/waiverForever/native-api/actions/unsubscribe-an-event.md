# Unsubscribe an Event with WaiverForever

Deletes a webhook subscription from WaiverForever.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/openapi/v1/webhooks/:subscription_id/`
- **Base URL:** `https://api.waiverforever.com`
- **Official documentation:** [Unsubscribe an Event](https://docs.waiverforever.com/#unsubscribe-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_id` | path | `string` | yes | Webhook subscription identifier. |
