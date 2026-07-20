# Update Space Properties with Qlik

Updates an existing space's properties in Qlik.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/spaces/:spaceId`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Update Space Properties](https://qlik.dev/apis/rest/spaces/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Qlik space ID. |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations array for updating the space. |
