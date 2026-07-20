# Get Collection with LinkTwin

Retrieves a collection and its items from LinkTwin.

## Endpoint

- **Method:** `GET`
- **Path:** `/collection/:id`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Get Collection](https://linktw.in/developers#get-single-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Collection ID. |
| `limit` | query | `number` | no | Per page data result. |
| `page` | query | `number` | no | Current page request. |
