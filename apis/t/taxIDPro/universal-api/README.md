# <img src="https://images.mindcloud.co/apps/icons/tax-id-pro-icon_1777931134903.png" alt="Tax ID Pro logo" width="28" height="28"> Tax ID Pro: Universal API

Validate individual, entity, and VAT tax identification numbers across more than 100 countries using the Tax ID Pro API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/taxIDPro/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://taxid.pro/
- **Vendor API docs:** https://taxid.pro/docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Tax ID](actions/validate-tax-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxIDPro/latest/actions/validate-tax-id?connectionId=$CONNECTION_ID&country=string&tin=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Tax Id Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Tax ID](actions/validate-tax-id.md) | GET | Retrieves a tax ID validation from Tax ID Pro. |

### Tax Id Validation Batch

| Action | Method | Description |
| --- | --- | --- |
| [Batch Validate Tax IDs](actions/batch-validate-tax-ids.md) | POST | Creates batch tax ID validations in Tax ID Pro. |

