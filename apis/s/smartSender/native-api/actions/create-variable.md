# Create Variable with Smart Sender

Creates a new variable in Smart Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/variables`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Create Variable](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676575629/Variables%2BAPI%2B-%2Ben)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional variable description. |
| `name` | body | `string` | yes | Unique variable name within the project. |
| `type` | body | `string` | yes | Variable type. |
