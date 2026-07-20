# Add Tags (Bulk) with Sequenzy

Adds tags to multiple subscribers in Sequenzy.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/tags/bulk`
- **Base URL:** `https://api.sequenzy.com/api/v1`
- **Official documentation:** [Add Tags (Bulk)](https://docs.sequenzy.com/api-reference/subscribers/tags/add-bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Subscriber email address. |
| `tags` | body | `list<string>` | yes | Tag names to add. |
