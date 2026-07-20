# Get SMS Status By API Message ID with TextingHouse

Retrieves TextingHouse SMS status by API message ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/do`
- **Base URL:** `https://api.textinghouse.com/http/v1`
- **Official documentation:** [Get SMS Status By API Message ID](https://www.textinghouse.com/en/api-sms-http/api-documentation/#doc-demstatut)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_id` | body | `string` | yes | TextingHouse API message identifier returned by a send action. |
