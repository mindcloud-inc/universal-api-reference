# Create Document with Mifiel

Creates a new document in Mifiel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/documents`
- **Base URL:** `https://app.mifiel.com`
- **Official documentation:** [Create Document](https://docs.mifiel.com/en/#tag/Document/operation/CreateDocument)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Document file in PDF format. |
| `signatories[]` | body | `array<object>` | no | List of signatories who will sign the document. |
| `signatories[].email` | body | `string` | yes | Signatory email address. |
| `signatories[].name` | body | `string` | no | Signatory full name. |
| `signatories[].tax_id` | body | `string` | no | Signatory tax ID (RFC in Mexico). |
| `signatories[].allowed_signature_methods[]` | body | `array<string>` | no | Allowed signature methods for the signatory: FEA, FESCV, or FESSV. |
| `days_to_expire` | body | `number` | no | Number of days before the document expires. |
| `external_id` | body | `string` | no | External ID for idempotency. |
| `send_invites` | body | `boolean` | no | Whether to send invitation emails automatically. |
| `remind_every` | body | `number` | no | How often to remind signers, in days. Supported values are 0, 1, 3, and 7. |
| `viewers[]` | body | `array<object>` | no | List of viewers who can access the document without signing. |
| `viewers[].email` | body | `string` | no | Viewer email address. |
| `viewers[].name` | body | `string` | no | Viewer full name. |
