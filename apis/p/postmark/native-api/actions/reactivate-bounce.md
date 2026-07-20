# Reactivate Bounce with Postmark

Reactivates a bounce in Postmark.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bounces/:bounceId/activate`
- **Base URL:** `https://api.postmarkapp.com`
- **Official documentation:** [Reactivate Bounce](https://postmarkapp.com/developer/api/bounce-api#activate-bounce)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bounceId` | path | `string` | yes | The Postmark bounce ID. |
