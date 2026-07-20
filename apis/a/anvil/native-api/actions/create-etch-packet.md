# Create Etch Packet with Anvil

Creates a new Etch packet in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Create Etch Packet](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createEtchPacket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.name` | body | `string` | no | Provide Name for Create Etch Packet. |
| `variables.organizationEid` | body | `string` | no | Provide Organization EID for Create Etch Packet. |
| `variables.isDraft` | body | `boolean` | no | Provide Is Draft for Create Etch Packet. |
| `variables.isTest` | body | `boolean` | no | Provide Is Test for Create Etch Packet. |
| `variables.files[]` | body | `array<object>` | no | Provide Files for Create Etch Packet. |
| `variables.signers[]` | body | `array<object>` | no | Provide Signers for Create Etch Packet. |
| `variables.signatureRecipients[]` | body | `array<object>` | no | Provide Signature Recipients for Create Etch Packet. |
| `variables.data` | body | `object` | no | Provide Data for Create Etch Packet. |
| `variables.replyToName` | body | `string` | no | Provide Reply To Name for Create Etch Packet. |
| `variables.replyToEmail` | body | `string` | no | Provide Reply To Email for Create Etch Packet. |
| `variables.signatureEmailSubject` | body | `string` | no | Provide Signature Email Subject for Create Etch Packet. |
| `variables.signatureEmailBody` | body | `string` | no | Provide Signature Email Body for Create Etch Packet. |
| `variables.signaturePageOptions` | body | `object` | no | Provide Signature Page Options for Create Etch Packet. |
| `variables.finishPageOptions` | body | `object` | no | Provide Finish Page Options for Create Etch Packet. |
| `variables.enableEmails` | body | `object` | no | Provide Enable Emails for Create Etch Packet. |
| `variables.createCastTemplatesFromUploads` | body | `boolean` | no | Provide Create Cast Templates From Uploads for Create Etch Packet. |
| `variables.duplicateCasts` | body | `boolean` | no | Provide Duplicate Casts for Create Etch Packet. |
| `variables.mergePDFs` | body | `boolean` | no | Provide Merge PDFs for Create Etch Packet. |
| `variables.allowUpdates` | body | `boolean` | no | Provide Allow Updates for Create Etch Packet. |
| `variables.webhookURL` | body | `string` | no | Provide Webhook URL for Create Etch Packet. |
| `variables.signatureProvider` | body | `string` | no | Provide Signature Provider for Create Etch Packet. |
| `variables.advancedCreate` | body | `boolean` | no | Provide Advanced Create for Create Etch Packet. |
| `variables.detectBoxesAdvanced` | body | `boolean` | no | Provide Detect Boxes Advanced for Create Etch Packet. |
