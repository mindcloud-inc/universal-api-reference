# Score IP Address with IPQS Fraud and Risk Scoring

Retrieves IP fraud and proxy risk details from IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ip/{apiKey}/:ip`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Score IP Address](https://www.ipqualityscore.com/documentation/proxy-detection-api/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | path | `string` | yes | IPv4 or IPv6 address to score. |
