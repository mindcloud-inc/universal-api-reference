# List Forms with Form.io

Retrieves forms from your Form.io project.

## Endpoint

- **Method:** `GET`
- **Path:** `/form`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [List Forms](https://help.form.io/developers/introduction/api-documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum number of forms to return. |
| `skip` | query | `string` | no | Number of forms to skip before returning results. |
