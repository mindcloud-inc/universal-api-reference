# Create Record Comment with NetHunt CRM

Creates a record comment in NetHunt CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/create-comment/:recordId`
- **Base URL:** `https://nethunt.com/api/v1/zapier`
- **Official documentation:** [Create Record Comment](https://nethunt.com/integration-api#create-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordId` | path | `string` | yes | Record ID to create the comment for. |
| `text` | body | `string` | yes | Comment text. |
