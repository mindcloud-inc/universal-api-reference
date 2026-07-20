# Send Credential with Certifier

Sends an existing credential from Certifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/credentials/:id/send`
- **Base URL:** `https://api.certifier.io/v1`
- **Official documentation:** [Send Credential](https://developers.certifier.io/docs/api-reference/credentials/send-a-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `deliveryMethod` | body | `string` | yes | Currently the only supported value is email. |
