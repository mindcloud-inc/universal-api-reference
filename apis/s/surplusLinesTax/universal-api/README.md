# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-26-at-18_1774560515664.png" alt="Surplus Lines Tax logo" width="28" height="28"> Surplus Lines Tax: Universal API

REST API for surplus lines tax calculations across all 50 U.S. states, DC, Puerto Rico, and the U.S. Virgin Islands, including stamping fees, regulatory charges, and historical rate lookups for insurance workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/surplusLinesTax/latest
- **Category:** Commerce / Accounting
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://surpluslinesapi.com
- **Vendor API docs:** https://surpluslinesapi.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Historical Surplus Lines Tax Rates](actions/retrieve-historical-surplus-lines-tax-rates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surplusLinesTax/latest/actions/retrieve-historical-surplus-lines-tax-rates?connectionId=$CONNECTION_ID&state=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Historical Rate

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Historical Surplus Lines Tax Rates](actions/retrieve-historical-surplus-lines-tax-rates.md) | GET |  |

### Tax Calculation

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Surplus Lines Taxes](actions/calculate-surplus-lines-taxes.md) | POST |  |

