# Create Token For User with MOBIDI

Creates a user access token in MOBIDI.

## Endpoint

- **Method:** `GET`
- **Path:** `/MobidiTokenHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Create Token For User](https://servis2.dece.com.tr/mobiditokenhandler?op=.wsdl&loginWithGuest=1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Username` | query | `string` | yes | MOBIDI username to mint a token for. |
| `Password` | query | `string` | yes | MOBIDI password paired with the username. |
| `tokenTarget` | query | `string` | yes | Target scope for the generated token. |
