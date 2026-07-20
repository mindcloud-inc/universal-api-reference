# Execute Template with Agilite

Executes a template in Agilite by profile key.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/execute`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Execute Template](https://docs.agilite.io/reference/execute-3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile-key` | query | `string` | yes | Template profile key. |
| `data` | body | `object` | yes | Payload passed to the template execution. |
