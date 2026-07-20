# Get Form Template with Fingertip

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/form-templates/:formTemplateId`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Get Form Template](https://docs.fingertip.com/openapi-specs/get-form-template.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formTemplateId` | path | `string` | yes | ID of the form template to retrieve. |
| `siteId` | query | `string` | yes | ID of the site that owns the form template. |
