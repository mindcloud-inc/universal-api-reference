# Create Account with ActiveCampaign

Creates a new account in ActiveCampaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Create Account](https://developers.activecampaign.com/reference/create-an-account-new)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account` | body | `object` | no |
| `account.name` | body | `string` | yes |
| `account.accountUrl` | body | `string` | no |
| `account.owner` | body | `number` | no |
| `account.fields[]` | body | `array<object>` | no |
