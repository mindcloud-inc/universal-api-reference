# Check Domain Health with verifi.email

Check a domain's email-authentication health and return SPF, DKIM, DMARC, and BIMI scores with recommendations.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/domain/check`
- **Base URL:** `https://api.verifi.email`
- **Official documentation:** [Check Domain Health](https://verifi.email/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain to inspect. |
| `selector` | query | `string` | no | Optional DKIM selector to test directly. |
