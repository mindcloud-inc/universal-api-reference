# Search Surveys with Startquestion

Searches surveys in Startquestion.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/search`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Search Surveys](https://help.startquestion.com/en/articles/5810076-surveys)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | no | Survey title filter. |
| `status` | query | `number` | no | Survey status code. |
| `type` | query | `number` | no | Survey type code. |
| `security_level` | query | `number` | no | Survey security level. |
