# Create a New Contact Card Link with Linkbreakers

Creates a new contact card link in Linkbreakers.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/links/contact`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Create a New Contact Card Link](https://linkbreakers.com/help/api/links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customDomainId` | body | `string` | no | The custom domain ID. |
| `fallbackDestination` | body | `string` | no | Optional fallback URL if vCard download fails. |
| `leadGoalDefinition` | body | `string` | no | The lead goal definition for the link. |
| `leadTargetDefinition` | body | `string` | no | The lead target definition for the link. |
| `metadata` | body | `object` | no | Map of string key-value metadata for the contact link. |
| `name` | body | `string` | no | The name of the link. |
| `qrcodeDesignId` | body | `string` | no | The QR code design ID. |
| `qrcodeTemplateId` | body | `string` | no | The QR code template ID. |
| `shortlink` | body | `string` | no | The shortlink slug for the link. |
| `tags[]` | body | `array<string>` | no | Tags to associate with the link. |
| `vcardData` | body | `object` | yes | Contact information payload for the vCard link. |
| `waitForQrcode` | body | `boolean` | no | Wait for QR code generation to complete. |
