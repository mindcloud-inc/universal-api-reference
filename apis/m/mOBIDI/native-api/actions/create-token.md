# Create Token with MOBIDI

Creates an access token in MOBIDI.

## Endpoint

- **Method:** `GET`
- **Path:** `/MobidiTokenHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Create Token](https://servis2.dece.com.tr/mobiditokenhandler?op=.wsdl&loginWithGuest=1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tokenTarget` | query | `string` | yes | Target scope for the generated token. |
