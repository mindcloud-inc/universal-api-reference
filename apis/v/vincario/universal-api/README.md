# <img src="https://images.mindcloud.co/apps/icons/vincario_1774460259444.png" alt="Vincario logo" width="28" height="28"> Vincario: Universal API

Decode VINs, check theft status, and estimate vehicle values

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vincario/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vincario.com/
- **Vendor API docs:** https://vincario.com/api-docs/3.2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vincario/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET |  |

### Oem Vin Lookup

| Action | Method | Description |
| --- | --- | --- |
| [OEM VIN Lookup](actions/oem-vin-lookup.md) | GET |  |

### Stolen Check

| Action | Method | Description |
| --- | --- | --- |
| [Stolen Check](actions/stolen-check.md) | GET |  |

### Value Lists

| Action | Method | Description |
| --- | --- | --- |
| [List Body Types](actions/list-body-types.md) | GET |  |
| [List Colors](actions/list-colors.md) | GET |  |
| [List Drive Types](actions/list-drive-types.md) | GET |  |
| [List Fuel Types](actions/list-fuel-types.md) | GET |  |
| [List Makes](actions/list-makes.md) | GET |  |
| [List Models](actions/list-models.md) | GET |  |
| [List Product Types](actions/list-product-types.md) | GET |  |
| [List Transmission Types](actions/list-transmission-types.md) | GET |  |
| [List Vehicles](actions/list-vehicles.md) | GET |  |

### Vehicle Market Value

| Action | Method | Description |
| --- | --- | --- |
| [Vehicle Market Value](actions/vehicle-market-value.md) | GET |  |

### Vin Decoder

| Action | Method | Description |
| --- | --- | --- |
| [VIN Decode](actions/vin-decode.md) | GET |  |
| [VIN Decode Info](actions/vin-decode-info.md) | GET |  |

