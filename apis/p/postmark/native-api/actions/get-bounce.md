# Get Bounce with Postmark

Retrieves a bounce from Postmark.

## Endpoint

- **Method:** `GET`
- **Path:** `/bounces/:bounceId`
- **Base URL:** `https://api.postmarkapp.com`
- **Official documentation:** [Get Bounce](https://postmarkapp.com/developer/api/bounce-api#single-bounce)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bounceId` | path | `string` | yes | The Postmark bounce ID. |
