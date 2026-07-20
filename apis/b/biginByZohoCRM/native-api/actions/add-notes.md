# Add Notes with Bigin by Zoho CRM

Creates standalone notes in Bigin by Zoho CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Notes`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Add Notes](https://www.bigin.com/developer/docs/apis/v2/create-notes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Array of note objects to create. Each note should include the target parent record and module. |
