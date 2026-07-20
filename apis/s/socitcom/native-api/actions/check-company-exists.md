# Check Company Exists with Société.com

Checks whether a company exists in Société.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/entreprise/:numid/exist`
- **Base URL:** `https://api.societe.com/api/v1`
- **Official documentation:** [Check Company Exists](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-existence-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numid` | path | `string` | no | Company identifier accepted by Société.com (SIREN, SIRET, VAT, or Société.com company id). |
