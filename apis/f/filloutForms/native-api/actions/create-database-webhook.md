# Create Database Webhook with Fillout Forms

Creates a database webhook in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/webhooks`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Create Database Webhook](https://www.fillout.com/help/database/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database. |
| `url` | body | `string` | yes | The URL to receive webhook POST requests. |
| `events[]` | body | `array<string>` | yes | Array of event types to subscribe to. |
| `tableId` | body | `string` | no | Optional table ID to filter events. Omit to receive events from all tables. |
