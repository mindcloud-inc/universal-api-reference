# List Form Submissions with Form.io

Retrieves submissions for a form in Form.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/form/:formId/submission`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [List Form Submissions](https://help.form.io/developers/introduction/api-documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form ID to list submissions for. |
| `limit` | query | `string` | no | Maximum submissions to return. |
| `skip` | query | `string` | no | Number of submissions to skip. |
