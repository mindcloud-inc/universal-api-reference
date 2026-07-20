# Create Postcard with PostGrid Print & Mail

Creates a postcard in PostGrid Print & Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/postcards`
- **Base URL:** `https://api.postgrid.com/print-mail/v1`
- **Official documentation:** [Create Postcard](https://postgrid.readme.io/reference/postcards_create-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | The recipient contact ID or recipient payload. |
| `size` | body | `string` | yes | The postcard size. |
| `frontHTML` | body | `string` | no | Inline HTML for the front of the postcard. |
| `backHTML` | body | `string` | no | Inline HTML for the back of the postcard. |
| `frontTemplate` | body | `string` | no | The template ID for the front of the postcard. |
| `backTemplate` | body | `string` | no | The template ID for the back of the postcard. |
| `pdf` | body | `string` | no | A two-page PDF source for the postcard. |
| `from` | body | `string` | no | The sender contact ID or sender payload. |
| `mergeVariables` | body | `object` | no | Template merge variables for the postcard. |
| `description` | body | `string` | no | An optional description visible in the API and dashboard. |
| `metadata` | body | `object` | no | Custom metadata for this postcard. |
| `sendDate` | body | `date` | no | Schedule the postcard for a future send date. |
| `mailingClass` | body | `string` | no | The mailing class for the postcard. |
| `paper` | body | `string` | no | Paper stock settings for the postcard. |
