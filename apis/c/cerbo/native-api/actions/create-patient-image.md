# Create Patient Image with Cerbo

Creates a new patient image in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/images`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Patient Image](https://docs.cer.bo/#tag/Patient-Images/operation/createPatientImage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `pt_id` | body | `number` | yes | An integer identifier for the patient associated with the document. |
| `mime_type` | body | `string` | yes | A string indicating the MIME type of the file. Valid MIME types: image/jpeg image/jpg image/gif image/png image/pngx |
| `base64_content` | body | `string` | yes | Binary data, encoded base64. Maximum file size is 16MB. |
