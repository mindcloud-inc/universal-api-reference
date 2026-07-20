# List Form Responses with Google Forms

Retrieves form responses from Google Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/:formId/responses`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [List Form Responses](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms.responses/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier to list responses from. |
| `submittedAfter` | query | `string` | no | Return responses submitted after this RFC3339 UTC timestamp, for example 2026-05-01T00:00:00Z. |
| `submittedAtOrAfter` | query | `string` | no | Return responses submitted at or after this RFC3339 UTC timestamp. |
| `filter` | query | `string` | no | Raw Google Forms response filter. Currently supports timestamp > N or timestamp >= N. |
