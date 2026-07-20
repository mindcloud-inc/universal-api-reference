# Verify Credentials with CommercioNetwork

Retrieves credential verification details from CommercioNetwork.

## Endpoint

- **Method:** `GET`
- **Path:** `/eKYC/:address`
- **Base URL:** `https://dev-api.commercio.app/v1`
- **Official documentation:** [Verify Credentials](https://docs.commercio.network/app_developers/commercioapi-ekyc.html#verify-credentials)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | path | `string` | yes | The Commercio DID or wallet address to inspect for eKYC status. |
