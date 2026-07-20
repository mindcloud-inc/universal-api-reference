# Get UK Address By SID with Hopewiser

## Endpoint

- **Method:** `GET`
- **Path:** `/atlaslive/json/:maf`
- **Base URL:** `https://cloud.hopewiser.com`
- **Official documentation:** [Get UK Address By SID](https://www.hopewiser.com/developer-document/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `maf` | path | `string` | yes | Hopewiser MAF identity. This tenant is provisioned for uk-rm-paf-mr. |
| `q` | query | `string` | yes | The literal decoded Hopewiser address SID to expand. MindCloud URL-encodes query arguments when sending the request. |
