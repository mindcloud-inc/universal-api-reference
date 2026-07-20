# Get Domain Cname Settings with Pinghome

Retrieves domain CNAME settings from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/statuspage-query/v1/domain/:domain/cname`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Get Domain Cname Settings](https://docs.pinghome.io/statuspages/get-domain-cname-settings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | no | The custom domain to inspect for CNAME settings. |
