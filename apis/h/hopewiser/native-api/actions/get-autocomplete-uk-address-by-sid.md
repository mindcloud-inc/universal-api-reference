# Get Autocomplete UK Address By SID with Hopewiser

## Endpoint

- **Method:** `GET`
- **Path:** `/autoc/json/:maf`
- **Base URL:** `https://cloud.hopewiser.com`
- **Official documentation:** [Get Autocomplete UK Address By SID](https://www.hopewiser.com/developer-document/autocomplete-rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `maf` | path | `string` | yes | Hopewiser MAF identity. This tenant is provisioned for uk-rm-paf-mr. |
| `q` | query | `string` | yes | The literal decoded Hopewiser autocomplete SID to expand. MindCloud URL-encodes query arguments when sending the request. |
