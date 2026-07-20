# Update card token with Nexiopay

## Endpoint

- **Method:** `PUT`
- **Path:** `/pay/v3/vault/card/{cardToken}`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Update card token](https://docs.nexiopay.com/reference/updatecardtoken)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardToken` | path | `string` | yes | Saved card token to update. |
| `card` | body | `object` | no | Updated card information object documented by Nexio. |
| `data` | body | `object` | no | Updated token metadata object documented by Nexio. |
| `shouldUpdateCard` | body | `boolean` | no | Whether Nexio should update card details for the token. |
