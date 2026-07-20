# Create Model with HeadshotPro

Creates a new model in HeadshotPro.

## Endpoint

- **Method:** `POST`
- **Path:** `/organization/models`
- **Base URL:** `https://server.headshotpro.com/api/v2`
- **Official documentation:** [Create Model](https://www.headshotpro.com/api/models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the user who should receive the HeadshotPro session. |
| `teamId` | body | `string` | no | Optional team assignment for the new model. |
| `version` | body | `string` | no | Optional model generation version. |
