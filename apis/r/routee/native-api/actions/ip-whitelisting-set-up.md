# IP whitelisting set up with Routee

Sets up API IP whitelisting in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/security/whitelist`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [IP whitelisting set up](https://docs.routee.net/reference/ip-whitelisting-set-up)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whitelistedIps[]` | body | `array<string>` | yes | [Required, not empty] An Array of valid ip’s that will be used as whitelisted for using the API for the specific application. |
