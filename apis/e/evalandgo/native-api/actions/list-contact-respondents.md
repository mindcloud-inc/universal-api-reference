# List Contact Respondents with Evalandgo

Retrieves respondents for a contact from Evalandgo.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/contacts/:contactId/respondents`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [List Contact Respondents](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1contacts~1{contactId}~1respondents/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Contact identifier |
| `email` | query | `string` | no | — |
| `firstName` | query | `string` | no | — |
| `lastName` | query | `string` | no | — |
| `finish` | query | `boolean` | no | — |
| `withResponse` | query | `string` | no | — |
| `order[startAt]` | query | `string` | no | — |
| `order[endAt]` | query | `string` | no | — |
| `order[id]` | query | `string` | no | — |
