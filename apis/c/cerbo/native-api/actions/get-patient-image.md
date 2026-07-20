# Get Patient Image with Cerbo

Retrieves patient image details from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/images/:image_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Patient Image](https://docs.cer.bo/#tag/Patient-Images/operation/showPatientImage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `image_id` | path | `number` | no | ID of image |
