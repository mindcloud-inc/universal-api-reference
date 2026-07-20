# List Database Webhooks with Fillout Forms

Retrieves database webhooks from Fillout.

## Endpoint

- **Method:** `GET`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/webhooks`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [List Database Webhooks](https://www.fillout.com/help/database/list-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database. |
