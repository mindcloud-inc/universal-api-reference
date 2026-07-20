# List Patient Images with Cerbo

Retrieves patient images from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/images`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Images](https://docs.cer.bo/#tag/Patient-Images/operation/listPatientImages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | ID of patient |
| `photo_type` | query | `string` | no | String (either “personal” or “medical”). If left blank, both types will be returned. |
