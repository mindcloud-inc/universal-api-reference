# List Form Responses with Fingertip

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/form-responses`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [List Form Responses](https://docs.fingertip.com/openapi-specs/list-form-responses.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formTemplateId` | query | `string` | yes | ID of the form template to list responses for. |
| `siteId` | query | `string` | yes | ID of the site that owns the form template. |
