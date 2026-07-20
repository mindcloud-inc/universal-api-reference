# Update Custom Field with UseINBOX

Updates an existing custom field in UseINBOX.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/inbox/v1/customfields/:id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Update Custom Field](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Custom field ID from INBOX. |
| `Name` | body | `string` | no | Updated custom field name. |
