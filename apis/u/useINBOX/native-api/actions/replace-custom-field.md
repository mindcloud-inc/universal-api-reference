# Replace Custom Field with UseINBOX

Replaces an existing custom field in UseINBOX.

## Endpoint

- **Method:** `PUT`
- **Path:** `/inbox/v1/customfields/:id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Replace Custom Field](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Custom field ID from INBOX. |
| `Name` | body | `string` | yes | Custom field name. |
| `Type` | body | `number` | yes | INBOX custom field type value. |
