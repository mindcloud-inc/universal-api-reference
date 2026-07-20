# Search Project Tasks with Everhour

Finds project tasks in Everhour by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/tasks/search`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [Search Project Tasks](https://everhour.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `projectId` | path | `string` | yes | Everhour project ID. |
| `query` | query | `string` | no | Task search query. |
| `searchInClosed` | query | `boolean` | no | Include closed tasks in the search results. |
