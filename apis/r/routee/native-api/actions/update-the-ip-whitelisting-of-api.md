# Update the IP whitelisting of API with Routee

Updates API IP whitelisting in Routee.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/security/whitelist`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Update the IP whitelisting of API](https://docs.routee.net/reference/update-the-ip-whitelisting-of-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whitelistedIps[]` | body | `array<string>` | yes | [Required, not empty] An Array of valid ip’s that will be used as whitelisted for using the API for the specific application. |
