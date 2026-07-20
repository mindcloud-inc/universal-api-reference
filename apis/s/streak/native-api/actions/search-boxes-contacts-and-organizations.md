# Search Boxes, Contacts, and Organizations with Streak

Finds boxes, contacts, and organizations in Streak by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/search`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Search Boxes, Contacts, and Organizations](https://streak.readme.io/reference/searching-for-boxes-contacts-and-organizations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search term used to find boxes, contacts, and organizations. |
| `pipelineKey` | query | `string<string>` | no | Limit box results to one or more pipelines. Send multiple values as a array. |
| `stageKey` | query | `string<string>` | no | Limit box results to one or more stages. Send multiple values as a array. |
