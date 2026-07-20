# Change Validation with Statsig

Creates a change validation in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/change_validation`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Change Validation](https://docs.statsig.com/api-reference/change-validation/change-validation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewID` | body | `string` | yes | Request body field. |
| `validated` | body | `boolean` | yes | Request body field. |
| `message` | body | `string` | no | Request body field. |
| `debugLinks` | body | `list` | no | Request body field. |
| `releasePipelineIDForCommit` | body | `string` | no | Request body field. |
