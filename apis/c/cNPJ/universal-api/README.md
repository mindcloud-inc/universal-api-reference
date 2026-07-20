# <img src="https://images.mindcloud.co/apps/icons/c-npj_1775856400228.png" alt="CNPJá logo" width="28" height="28"> CNPJá: Universal API

CNPJá provides real-time Brazilian CNPJ and registry lookup APIs for company offices, companies, people, ZIP codes, tax certificates, and credit balance checks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cNPJ/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cnpja.com
- **Vendor API docs:** https://cnpja.com/en/api/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Office by Tax ID](actions/get-office-by-tax-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cNPJ/latest/actions/get-office-by-tax-id?connectionId=$CONNECTION_ID&taxId=37335118000180" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Office by Tax ID](actions/get-office-by-tax-id.md) | GET | Retrieves office details by tax ID from CNPJá. |
| [Get Office Geocoding](actions/get-office-geocoding.md) | GET | Retrieves office geocoding details from CNPJá. |
| [Get Office State Registrations](actions/get-office-state-registrations.md) | GET | Retrieves office state registrations from CNPJá. |
| [Get Office SUFRAMA](actions/get-office-suframa.md) | GET | Retrieves office SUFRAMA details from CNPJá. |
| [Get Office Tax Regime](actions/get-office-tax-regime.md) | GET | Retrieves office tax regime details from CNPJá. |

