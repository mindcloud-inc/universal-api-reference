# Create Recipient Account with Trolley

Creates a new recipient payment account in Trolley.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/recipients/:id/accounts`
- **Base URL:** `https://api.trolley.com`
- **Official documentation:** [Create Recipient Account](https://developers.trolley.com/api/#create-account)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `type` | body | `string` | yes |
| `emailAddress` | body | `string` | yes |
