# Request SPID Session with CommercioNetwork

Creates a SPID session in CommercioNetwork.

## Endpoint

- **Method:** `POST`
- **Path:** `/eKYC/spid`
- **Base URL:** `https://dev-api.commercio.app/v1`
- **Official documentation:** [Request SPID Session](https://docs.commercio.network/app_developers/commercioapi-ekyc.html#request-spid-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `success_url` | body | `string` | yes | URL that Commercio should redirect to after a successful SPID authentication. |
