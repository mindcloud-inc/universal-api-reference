# Get Cart Abandonment with Soundee

Retrieves an abandoned cart from Soundee by ID or token.

## Endpoint

- **Method:** `GET`
- **Path:** `/cart-abandonments/:idOrToken`
- **Base URL:** `https://api.soundee.com/me`
- **Official documentation:** [Get Cart Abandonment](https://soundee.readme.io/reference/get-abandoned-cart-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrToken` | path | `string` | yes | The ID or token of the abandoned cart. |
