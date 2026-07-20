# Update Account with ActiveCampaign

Updates an existing account in ActiveCampaign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:id`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Update Account](https://developers.activecampaign.com/reference/update-an-account-new)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The account ID. |
| `account` | body | `object` | no | — |
| `account.name` | body | `string` | no | — |
| `account.accountUrl` | body | `string` | no | — |
| `account.fields[]` | body | `array<object>` | no | — |
| `account.owner` | body | `number` | no | — |
