# List Incident Actions with Pinghome

Retrieves incident actions from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/incident-query/v1/incident/:id/actions`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [List Incident Actions](https://docs.pinghome.io/incident-management/incident-tracking/get-incident-actions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The incident ID. |
