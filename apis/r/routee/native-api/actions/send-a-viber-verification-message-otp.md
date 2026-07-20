# Send a Viber Verification Message (OTP) with Routee

Sends a Viber verification message (OTP) with Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/viber/otp`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send a Viber Verification Message (OTP)](https://docs.routee.net/reference/viber-otp-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `senderInfoTrackingId` | body | `string` | yes | Unique identifier of the Viber sender (from your sender configuration). Used for routing and tracking |
| `to[]` | body | `array<string>` | no | Recipient phone number in **E.164** format (e.g. `+306912345678`). Must include `+` and country code |
| `ttl` | body | `number` | no | Time-to-live in **seconds** for the OTP delivery attempt |
| `seq` | body | `string` | no | Your own sequence or correlation ID for this request (e.g. for linking request and response or callbacks) |
| `label` | body | `string` | no | Message label. Allowed values: `transactional`, `promotional` |
| `type` | body | `string` | no | OTP message type. Allowed values: `PRIMARY_ONLY`, `ALL_DEVICE` |
| `templateId` | body | `string` | no | ID of the OTP template to use. See [Templates inventory](https://docs.routee.net/docs/templates-inventory) |
| `templateParams` | body | `object` | no | Key-value map of template variables. Keys in **camelCase** (e.g. `pin`, `businessPlatformName`, `codeValidityTime`). See [Template variables validation](https://docs.routee.net/docs/template-variables-validations) |
| `templateLang` | body | `string` | no | Language of the template (ISO 639-1, e.g. `en`, `el`). See [Localization](https://docs.routee.net/docs/localization) |
