# List Inboxes with Rossum

Retrieves inboxes from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [List Inboxes](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_prefix` | query | `string` | no | Filter inboxes by email prefix. |
| `ordering` | query | `string` | no | Ordering expression, for example name or -name. |
