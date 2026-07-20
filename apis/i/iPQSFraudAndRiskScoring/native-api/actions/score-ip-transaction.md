# Score IP Transaction with IPQS Fraud and Risk Scoring

Retrieves transaction risk scoring for an IP from IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ip/{apiKey}/:ip`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Score IP Transaction](https://www.ipqualityscore.com/documentation/proxy-detection-api/transaction-scoring)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | path | `string` | yes | IPv4 or IPv6 address to score. |
| `billing_email` | query | `string` | no | Customer billing email address used as transaction scoring context. |
| `billing_country` | query | `string` | no | Customer billing country name or ISO-Alpha2 country code. |
| `billing_phone` | query | `string` | no | Customer billing phone number used as transaction scoring context. |
