# List Webhooks with Documo

Retrieves webhook endpoint records from Documo.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [List Webhooks](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | Account UUID to filter webhooks. |
| `numberId` | query | `string` | no | Fax number UUID to filter webhooks. |
