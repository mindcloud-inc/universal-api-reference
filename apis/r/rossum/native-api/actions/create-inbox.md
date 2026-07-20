# Create Inbox with Rossum

Creates a new inbox in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Create Inbox](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the inbox to create. |
| `email_prefix` | body | `string` | yes | Email prefix used to generate the Rossum inbox address. |
| `queue` | body | `string` | yes | Queue URL that should receive inbox documents. |
