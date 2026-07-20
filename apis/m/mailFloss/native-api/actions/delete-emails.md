# Delete Emails with MailFloss

Deletes email addresses from MailFloss privacy storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/delete`
- **Base URL:** `https://api.mailfloss.com`
- **Official documentation:** [Delete Emails](https://developers.mailfloss.com/privacy-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Email addresses to delete from MailFloss data privacy storage. |
