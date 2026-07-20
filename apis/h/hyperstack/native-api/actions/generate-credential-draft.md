# Generate Credential Draft with Hyperstack Certificates

## Endpoint

- **Method:** `POST`
- **Path:** `/credentials/generate`
- **Base URL:** `https://api.thehyperstack.com/v1`
- **Official documentation:** [Generate Credential Draft](https://thehyperstack.com/docs/api-guide/generate-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipient.name` | body | `string` | yes | Recipient full name for the draft credential. |
| `recipient.email` | body | `string` | yes | Recipient email for the draft credential. |
| `group_key` | body | `string` | yes | Credential group key used to generate the draft. |
