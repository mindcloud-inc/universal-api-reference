# Create Database Webhook with Fillout

Creates a database webhook in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/webhooks`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Create Database Webhook](https://fillout.com/help/database/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database identifier. |
| `url` | body | `string` | yes | The webhook destination URL. |
| `events[]` | body | `array<string>` | yes | The webhook events to subscribe to. |
| `tableId` | body | `string` | no | Optional table identifier to scope the webhook. |
