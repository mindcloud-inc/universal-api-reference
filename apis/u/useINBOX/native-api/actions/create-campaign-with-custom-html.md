# Create Campaign With Custom HTML with UseINBOX

Creates a campaign from custom HTML in UseINBOX.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/v1/campaigns/custom`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Create Campaign With Custom HTML](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `senderAccountId` | body | `string` | yes | Sender account ID used for the campaign. |
| `listType` | body | `number` | yes | INBOX list type value for the campaign audience. |
| `lists[]` | body | `array<string>` | yes | Contact list IDs that should receive the campaign. Send multiple values as a array. |
| `subject` | body | `string` | yes | Subject line for the custom HTML campaign. |
| `htmlContent` | body | `string` | yes | HTML content for the campaign. |
| `language` | body | `string` | yes | Campaign language code such as en-US. |
