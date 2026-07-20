# List Knowledge Base Structure with Usedesk

Retrieves knowledge base directories and categories from Usedesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/support/:account_id/list`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [List Knowledge Base Structure](https://api.usedocs.com/article/51398)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Knowledge base ID in the system. |
