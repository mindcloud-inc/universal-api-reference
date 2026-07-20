# Update Newsletter with UseINBOX

Updates an existing newsletter in UseINBOX.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/inbox/v1/newsletters/:id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Update Newsletter](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Newsletter ID from INBOX. |
| `subject` | body | `string` | no | Updated newsletter subject. |
