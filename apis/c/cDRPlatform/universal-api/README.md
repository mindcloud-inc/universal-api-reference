# <img src="https://images.mindcloud.co/apps/icons/c-drplatform_1776171606519.png" alt="CDR Platform logo" width="28" height="28"> CDR Platform: Universal API

Price, purchase, and verify carbon removal orders

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cDRPlatform/latest
- **Category:** Commerce / Procurement
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cdrplatform.com
- **Vendor API docs:** https://cdrplatform.com/docs/open-api-schema

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Calculate CO2 Removal Price](actions/calculate-co2-removal-price.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cDRPlatform/latest/actions/calculate-co2-removal-price?connectionId=$CONNECTION_ID&weightUnit=kg&currency=usd&items%5B%5D.methodType=forestation&items%5B%5D.cdrAmount=1000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Cdr Certificate

| Action | Method | Description |
| --- | --- | --- |
| [Get CDR Certificate By ID](actions/get-cdr-certificate-by-id.md) | GET | Retrieves a CDR certificate by ID from CDR Platform. |

### Co2 Removal Price

| Action | Method | Description |
| --- | --- | --- |
| [Calculate CO2 Removal Price](actions/calculate-co2-removal-price.md) | GET | Calculates CO2 removal pricing in CDR Platform. |

### Co2 Removal Purchase

| Action | Method | Description |
| --- | --- | --- |
| [Purchase CO2 Removal](actions/purchase-co2-removal.md) | POST | Creates a CO2 removal purchase in CDR Platform. |

