# Create Camio with Camio

Creates a Camio in Camio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/me/camios`
- **Base URL:** `https://camio.com/api`
- **Official documentation:** [Create Camio](https://api.camio.com/#create-camio)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional name for the Camio link. |
| `query` | body | `object` | yes | The Camio query object, for example `{ "text": "today 6am to 7am apps@mindcloud.co" }`. |
| `type` | body | `string` | no | Optional Camio type, usually `private` or `public`. |
