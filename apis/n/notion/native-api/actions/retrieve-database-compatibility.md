# Retrieve Database (Compatibility) with Notion

Retrieves a database from Notion's compatibility endpoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/databases/:database_id`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Retrieve Database (Compatibility)](https://developers.notion.com/reference/retrieve-a-database)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Notion-Version` | `2025-09-03` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_id` | path | `string` | yes | ID of the database. |
