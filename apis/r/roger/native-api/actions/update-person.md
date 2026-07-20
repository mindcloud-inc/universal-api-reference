# Update Person with Roger

## Endpoint

- **Method:** `PATCH`
- **Path:** `/people/:id`
- **Base URL:** `https://api.rogerroger.io`
- **Official documentation:** [Update Person](https://developer.rogerroger.io/crm/people)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Person identifier. |
| `givenName` | body | `string` | yes | Updated given name for the person. |
