# <img src="https://images.mindcloud.co/apps/icons/ecologi_1773868619948.png" alt="Ecologi logo" width="28" height="28"> Ecologi: Universal API

Fund climate action and report environmental impact

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ecologi/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ecologi.com
- **Vendor API docs:** https://docs.ecologi.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Total Number of Trees](actions/get-total-number-of-trees.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/get-total-number-of-trees?connectionId=$CONNECTION_ID&username=business-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Carbon Avoidance

| Action | Method | Description |
| --- | --- | --- |
| [Get Total Tonnes of CO2e Avoided](actions/get-total-tonnes-of-co2e-avoided.md) | GET | Retrieves total CO2e avoided from Ecologi. |
| [Purchase Carbon Avoidance](actions/purchase-carbon-avoidance.md) | POST | Purchases carbon avoidance through Ecologi. |

### Carbon Removal

| Action | Method | Description |
| --- | --- | --- |
| [Get Total Tonnes of CO2e Removed](actions/get-total-tonnes-of-co2e-removed.md) | GET | Retrieves total CO2e removed from Ecologi. |
| [Purchase Carbon Removals](actions/purchase-carbon-removals.md) | POST | Purchases carbon removals through Ecologi. |

### Habitat Restoration

| Action | Method | Description |
| --- | --- | --- |
| [Get Total Habitat Restored](actions/get-total-habitat-restored.md) | GET | Retrieves total habitat restored from Ecologi. |
| [Purchase Habitat Restoration](actions/purchase-habitat-restoration.md) | POST | Purchases habitat restoration through Ecologi. |

### Impact

| Action | Method | Description |
| --- | --- | --- |
| [Get Total Impact](actions/get-total-impact.md) | GET | Retrieves total impact from Ecologi. |

### Trees

| Action | Method | Description |
| --- | --- | --- |
| [Get Total Number of Trees](actions/get-total-number-of-trees.md) | GET | Retrieves total trees planted from Ecologi. |
| [Purchase Trees](actions/purchase-trees.md) | POST | Purchases trees through Ecologi. |

