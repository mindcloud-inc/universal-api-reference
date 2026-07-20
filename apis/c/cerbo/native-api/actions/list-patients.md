# List Patients with Cerbo

Retrieves patient records from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patients](https://docs.cer.bo/#tag/Patients/operation/listPatients)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `boolean` | no | If this parameter is set it will only include ACTIVE patients |
