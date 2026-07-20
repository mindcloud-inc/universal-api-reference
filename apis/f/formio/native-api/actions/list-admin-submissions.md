# List Admin Submissions with Form.io

Retrieves admin submissions from your Form.io project.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/submission`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [List Admin Submissions](https://help.form.io/developers/introduction/api-documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum submissions to return. |
| `skip` | query | `string` | no | Number of submissions to skip. |
