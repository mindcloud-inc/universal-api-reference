# Create Custom Field with UseINBOX

Creates a custom field in UseINBOX.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/v1/customfields`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Create Custom Field](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Custom field name. |
| `Type` | body | `number` | yes | INBOX custom field type value. |
