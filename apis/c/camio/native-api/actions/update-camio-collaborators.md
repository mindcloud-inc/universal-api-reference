# Update Camio Collaborators with Camio

Updates Camio collaborators in Camio.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/me/camios`
- **Base URL:** `https://camio.com/api`
- **Official documentation:** [Update Camio Collaborators](https://api.camio.com/#update-a-camio)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The Camio id to update. |
| `collaborators` | body | `object` | yes | A collaborators object that restricts Camio access. |
