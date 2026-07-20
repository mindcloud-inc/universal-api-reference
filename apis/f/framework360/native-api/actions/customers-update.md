# Update Customer with Framework360

## Endpoint

- **Method:** `POST`
- **Path:** `customers/update`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [Update Customer](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Customer ID to update. |
| `nome` | body | `string` | no | Customer first name. |
| `cognome` | body | `string` | no | Customer last name. |
| `email` | body | `string` | no | Customer email address. |
| `password` | body | `string` | no | New customer password. |
| `telefono` | body | `string` | no | Customer phone number. |
| `ragione_sociale` | body | `string` | no | Billing company name. |
| `piva` | body | `string` | no | VAT number. |
| `cf` | body | `string` | no | Tax code. |
| `pec` | body | `string` | no | Certified email address. |
| `sdi` | body | `string` | no | SDI code. |
| `indirizzo` | body | `string` | no | Billing address. |
| `stato` | body | `string` | no | Country. |
| `citta` | body | `string` | no | City. |
| `comune` | body | `string` | no | Municipality. |
| `cap` | body | `string` | no | Postal code. |
