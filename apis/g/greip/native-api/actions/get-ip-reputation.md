# Get IP Reputation with Greip - Fraud Prevention

Retrieves IP reputation data from Greip.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/ip/threats`
- **Base URL:** `https://greipapi.com`
- **Official documentation:** [Get IP Reputation](https://docs.greip.io/api-reference/endpoint/scoring/ip-reputation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | yes | The IPv4 or IPv6 address to check for reputation and threat indicators. |
