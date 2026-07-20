# Create Transaction Event with Tiliter

Creates a transaction event in the Tiliter Recognition API.

## Endpoint

- **Method:** `POST`
- **Path:** `/recognition/:recognition_id/transaction_events`
- **Base URL:** `https://recognition.services.tiliter.com/v1/15`
- **Official documentation:** [Create Transaction Event](https://developer.tiliter.com/reference/create_transaction_event)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recognition_id` | path | `string` | yes |
| `type` | body | `string` | yes |
| `time` | body | `date` | yes |
| `detail` | body | `string` | yes |
