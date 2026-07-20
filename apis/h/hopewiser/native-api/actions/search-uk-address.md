# Search UK Address with Hopewiser

## Endpoint

- **Method:** `GET`
- **Path:** `/atlaslive/json/:maf`
- **Base URL:** `https://cloud.hopewiser.com`
- **Official documentation:** [Search UK Address](https://www.hopewiser.com/developer-document/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `maf` | path | `string` | yes | Hopewiser MAF identity. This tenant is provisioned for uk-rm-paf-mr. |
| `q` | query | `string` | yes | Address search criteria, postcode, partial address, or a Hopewiser Sid returned by a previous lookup. |
