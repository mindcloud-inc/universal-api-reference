# Download Search CSV with Powrbot

Retrieves CSV output for a Powrbot bulk search.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/:searchId/download/`
- **Base URL:** `https://powrbot.com/api/v1`
- **Official documentation:** [Download Search CSV](https://powrbot.com/cpages/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchId` | path | `number` | yes | Numeric search job identifier. |
