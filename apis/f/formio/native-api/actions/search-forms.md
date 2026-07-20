# Search Forms with Form.io

Finds forms in Form.io by title pattern.

## Endpoint

- **Method:** `GET`
- **Path:** `/form`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Search Forms](https://help.form.io/developers/introduction/api-documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum number of matching forms to return. |
| `skip` | query | `string` | no | Number of matching forms to skip before returning results. |
| `title__regex` | query | `string` | no | Regex filter applied to the form title. |
