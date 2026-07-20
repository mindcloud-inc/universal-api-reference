# Load Free Certificate with BunnyCDN

Loads a free certificate in BunnyCDN.

## Endpoint

- **Method:** `GET`
- **Path:** `/pullzone/loadFreeCertificate`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Load Free Certificate](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | query | `string` | yes | The hostname that the certificate should be loaded for. |
