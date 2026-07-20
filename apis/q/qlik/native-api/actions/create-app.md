# Create App with Qlik

Creates a new app in Qlik.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/apps`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Create App](https://qlik.dev/apis/rest/apps/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the new Qlik app. |
