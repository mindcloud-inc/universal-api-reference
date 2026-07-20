# Send Custom Input Field Message with Kommunicate

Creates a custom input field message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send Custom Input Field Message](https://docs.kommunicate.io/docs/message-types#custom-input-field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `groupId` | body | `string` | yes |
| `message` | body | `string` | yes |
| `fromUserName` | body | `string` | yes |
| `label` | body | `string` | yes |
| `field` | body | `string` | yes |
| `fieldType` | body | `string` | yes |
| `placeholder` | body | `string` | yes |
| `updateUserDetails` | body | `boolean` | yes |
| `validationRegex` | body | `string` | no |
| `validationErrorText` | body | `string` | no |
| `triggerEvent` | body | `string` | no |
