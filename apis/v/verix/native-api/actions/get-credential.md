# Get Credential with Verix

Retrieves a credential from your Verix account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/credentials/:credential_id/`
- **Base URL:** `https://api.verix.io`
- **Official documentation:** [Get Credential](https://docs.verix.io/verifiable_credentials_apis/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credential_id` | path | `string` | yes | Credential ID to retrieve. |
| `format` | query | `string` | no | Set to json_input for nested JSON output. Default is csv_input. Accepted values: `0`, `1`. |
