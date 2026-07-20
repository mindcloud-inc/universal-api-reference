# List Assignments with Innform

Retrieves assignments from Innform.

## Endpoint

- **Method:** `GET`
- **Path:** `/assignments`
- **Base URL:** `https://api.innform.io/v1`
- **Official documentation:** [List Assignments](https://innform.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional assignment status filter. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
