# List User Submissions with Form.io

Retrieves user submissions from your Form.io project.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/submission`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [List User Submissions](https://help.form.io/developers/introduction/api-documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum submissions to return. |
| `skip` | query | `string` | no | Number of submissions to skip. |
