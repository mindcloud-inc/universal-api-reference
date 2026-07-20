# Create Journal Entry with Lunatask

## Endpoint

- **Method:** `POST`
- **Path:** `/journal_entries`
- **Base URL:** `https://api.lunatask.app/v1`
- **Official documentation:** [Create Journal Entry](https://lunatask.app/api/journal-api/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_on` | body | `date` | yes | ISO-8601 formatted date for the journal entry |
| `name` | body | `string` | no | The name for the journal entry |
| `content` | body | `string` | yes | The content of the journal entry in Markdown |
