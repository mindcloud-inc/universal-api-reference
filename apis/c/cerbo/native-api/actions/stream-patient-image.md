# Stream Patient Image with Cerbo

Streams patient image content from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/images/:image_id/stream`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Stream Patient Image](https://docs.cer.bo/#tag/Patient-Images/operation/streamPatientImage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `image_id` | path | `number` | no | ID of image |
