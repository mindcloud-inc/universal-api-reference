# Search Tasks with Everhour

Finds tasks in Everhour by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/search`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [Search Tasks](https://everhour.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `query` | query | `string` | no | Task search query. |
| `searchInClosed` | query | `boolean` | no | Include closed tasks in the search results. |
