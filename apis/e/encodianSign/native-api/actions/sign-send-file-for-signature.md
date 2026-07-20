# Sign - Send File For Signature with Encodian - Sign

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Sign/EnvelopeCreateSingle`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Sign - Send File For Signature](https://support.encodian.com/hc/en-gb/articles/26845003436828-Envelope-Send-File-for-Signature)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Set the name of the envelope. |
| `sender` | body | `string` | yes | Email address of the licensed sender for the workspace. |
| `file` | body | `string` | yes | Base64-encoded file content to submit for signature. |
| `message` | body | `string` | no | Message to share with recipients. |
| `fileName` | body | `string` | no | Optional filename for the submitted file. |
| `labels[]` | body | `array<string>` | no | Labels to assign to the envelope. |
