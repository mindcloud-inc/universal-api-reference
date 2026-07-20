# Get Patient Image Content with Cerbo

Retrieves raw patient image content from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/images/:image_id/content`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Patient Image Content](https://docs.cer.bo/#tag/Patient-Images/operation/showPatientImageContent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `image_id` | path | `number` | no | ID of image |
