# Update Account with Zoho Desk

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/[:accountId]`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [Update Account](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Account.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | The Zoho Desk account ID. |
| `website` | body | `string` | no | Updated website for the account. |
