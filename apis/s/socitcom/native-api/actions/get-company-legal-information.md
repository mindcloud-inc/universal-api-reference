# Get Company Legal Information with Société.com

Retrieves company legal information from Société.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/entreprise/:numid/infoslegales`
- **Base URL:** `https://api.societe.com/api/v1`
- **Official documentation:** [Get Company Legal Information](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-informations-l&eacute;gales-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numid` | path | `string` | no | Company identifier accepted by Société.com (SIREN, SIRET, VAT, or Société.com company id). |
