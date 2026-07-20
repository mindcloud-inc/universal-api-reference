# Create Credential Interaction with Certifier

Creates a credential interaction in Certifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/credential-interactions`
- **Base URL:** `https://api.certifier.io/v1`
- **Official documentation:** [Create Credential Interaction](https://developers.certifier.io/docs/api-reference/credential-interactions/create-a-credential-interaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credentialId` | body | `string` | yes | — |
| `eventType` | body | `string` | yes | Use one of Certifier's documented interaction event values. |
| `triggeredBy` | body | `string` | yes | Use recipient or guest. |
| `triggeredAt` | body | `date` | yes | Use an ISO 8601 date-time string. |
