# List Campaigns with SmartReach

Retrieves campaigns from SmartReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [List Campaigns](https://help.smartreach.io/reference/getcampaigns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | — |
| `name` | query | `string` | no | — |
| `sender_email` | query | `string` | no | email of the sending email account |
| `receiver_email` | query | `string` | no | email of the receiving email account |
| `older_than` | query | `number` | no | timestamp in unix epoch milliseconds |
| `newer_than` | query | `number` | no | timestamp in unix epoch milliseconds |
