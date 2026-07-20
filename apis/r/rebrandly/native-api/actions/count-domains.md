# Count Domains with Rebrandly

Retrieves the number of domains in Rebrandly.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/count`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Count Domains](https://developers.rebrandly.com/docs/counting-your-domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | Filter by whether the domain can currently be used to brand links. |
| `type` | query | `string` | no | Filter domains by type. |
