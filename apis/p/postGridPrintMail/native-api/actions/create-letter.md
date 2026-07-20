# Create Letter with PostGrid Print & Mail

Creates a letter in PostGrid Print & Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/letters`
- **Base URL:** `https://api.postgrid.com/print-mail/v1`
- **Official documentation:** [Create Letter](https://postgrid.readme.io/reference/letters_create-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | The recipient contact ID or recipient payload. |
| `from` | body | `string` | no | The sender contact ID or sender payload. |
| `html` | body | `string` | no | Inline HTML content for the letter. |
| `template` | body | `string` | no | The PostGrid template ID to use for the letter. |
| `pdf` | body | `string` | no | A PDF URL or PDF source for the letter. |
| `mergeVariables` | body | `object` | no | Template merge variables for the letter. |
| `description` | body | `string` | no | An optional description visible in the API and dashboard. |
| `metadata` | body | `object` | no | Custom metadata for this letter. |
| `sendDate` | body | `date` | no | Schedule the letter for a future send date. |
| `mailingClass` | body | `string` | no | The mailing class for the letter. |
| `size` | body | `string` | no | The page size for the letter. |
| `addressPlacement` | body | `string` | no | How to place the address window content. |
| `doubleSided` | body | `boolean` | no | Print the letter double sided. |
| `color` | body | `boolean` | no | Print the letter in color. |
| `perforatedPage` | body | `number` | no | The page number to perforate for the letter. |
| `envelope` | body | `string` | no | Envelope settings for the letter. |
| `returnEnvelope` | body | `string` | no | The return-envelope configuration for the letter. |
| `attachedPDF` | body | `object` | no | Attach an additional PDF to the letter. |
| `plasticCard` | body | `object` | no | Plastic card settings for the letter. |
