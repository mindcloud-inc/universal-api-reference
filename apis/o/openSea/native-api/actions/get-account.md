# Get OpenSea Account Profile with OpenSea

Retrieves an OpenSea account profile.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/accounts/{address_or_username}`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get OpenSea Account Profile](https://docs.opensea.io/reference/get_account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_or_username` | path | `string` | yes | The blockchain address or username of the account to retrieve |
