# Legal Accept with Paycove

Creates a legal acceptance token in Paycove.

## Endpoint

- **Method:** `POST`
- **Path:** `accounts/legal-accept`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Legal Accept](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accepter_email` | body | `string` | yes | The email address accepting the legal terms. |
| `return_url` | body | `string` | yes | Where the signer returns after accepting the legal terms. |
| `state` | body | `string` | no | Optional opaque state value to round-trip through the acceptance flow. |
