# Create Recipient with Trolley

Creates a new recipient in Trolley.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/recipients`
- **Base URL:** `https://api.trolley.com`
- **Official documentation:** [Create Recipient](https://developers.trolley.com/api/#create-a-recipient)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | body | `string` | yes |
| `email` | body | `string` | yes |
| `firstName` | body | `string` | yes |
| `lastName` | body | `string` | yes |
