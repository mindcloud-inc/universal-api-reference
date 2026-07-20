# List Templates with Postmark

Retrieves templates from Postmark.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates`
- **Base URL:** `https://api.postmarkapp.com`
- **Official documentation:** [List Templates](https://postmarkapp.com/developer/api/templates-api#list-templates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LayoutTemplate` | query | `string` | no | Filter templates by layout template alias. |
