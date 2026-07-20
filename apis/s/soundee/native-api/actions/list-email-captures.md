# List Email Captures with Soundee

Retrieves captured email records from Soundee.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-captures`
- **Base URL:** `https://api.soundee.com/me`
- **Official documentation:** [List Email Captures](https://soundee.readme.io/reference/read-2)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_type` | query | `string` | no | Filter email captures by source type. |
| `q` | query | `string` | no | Search captures by email, first name, last name, or phone. |
