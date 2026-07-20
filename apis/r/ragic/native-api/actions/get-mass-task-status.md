# Get Mass Task Status with Ragic

Retrieves mass task status from Ragic.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Get Mass Task Status](https://www.ragic.com/docs/api/en/#tag/mass-operations/Task-Progress-Tracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | query | `string` | yes | UUID returned by a Ragic mass operation. |
