# List Email Lists with Mailcoach

Retrieves all email lists from Mailcoach.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-lists`
- **Base URL:** `https://mindcloud.mailcoach.app/api`
- **Official documentation:** [List Email Lists](https://www.mailcoach.app/api-documentation/endpoints/email-lists/)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[name]` | query | `string` | no | Filter email lists by exact name. |
| `filter[search]` | query | `string` | no | Search email lists by name. |
