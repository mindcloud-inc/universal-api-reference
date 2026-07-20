# Get Campaign Send Status with Dotdigital

Retrieves a campaign send status from Dotdigital by send ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/campaigns/send/:id`
- **Base URL:** `https://r2-api.dotmailer.com`
- **Official documentation:** [Get Campaign Send Status](https://developer.dotdigital.com/reference/get-campaign-send-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The GUID returned by the send campaign call. |
