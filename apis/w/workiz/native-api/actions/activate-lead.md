# Activate Lead with Workiz

Activates an existing lead in Workiz.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead/activate/:UUID/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [Activate Lead](https://developer.workiz.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UUID` | path | `string` | yes | The lead's UUID. |
