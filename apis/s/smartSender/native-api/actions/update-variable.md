# Update Variable with Smart Sender

Updates an existing variable in Smart Sender.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/variables/:variableId`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Update Variable](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676575629/Variables%2BAPI%2B-%2Ben)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated variable description. |
| `name` | body | `string` | yes | Required updated variable name. Smart Sender rejects updates without it. |
| `type` | body | `string` | no | Updated variable type. |
| `variableId` | path | `string` | yes | The Smart Sender variable ID. |
