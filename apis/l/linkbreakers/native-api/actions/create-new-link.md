# Create a New Link with Linkbreakers

Creates a new link in Linkbreakers.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/links`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Create a New Link](https://linkbreakers.com/help/api/links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversionTracking` | body | `boolean` | no | Enable conversion tracking by preserving lbid in the redirect URL. |
| `customDomainId` | body | `string` | no | The custom domain ID. |
| `destination` | body | `string` | yes | The destination URL to shorten. |
| `directoryId` | body | `string` | no | Directory to organize the link into. |
| `fallbackDestination` | body | `string` | no | Fallback destination URL to use when workflow steps are broken. |
| `leadGoalDefinition` | body | `string` | no | The lead goal definition for the link. |
| `leadTargetDefinition` | body | `string` | no | The lead target definition for the link. |
| `metadata` | body | `object` | no | Map of string key-value metadata for the link. |
| `name` | body | `string` | no | The name of the link. |
| `qrcodeDesignId` | body | `string` | no | The QR code design ID. |
| `qrcodeTemplateId` | body | `string` | no | The QR code template ID. |
| `shortlink` | body | `string` | no | The shortlink slug for the link. |
| `tags[]` | body | `array<string>` | no | Tags to associate with the link. |
| `waitForQrcode` | body | `boolean` | no | Wait for QR code generation to complete. |
