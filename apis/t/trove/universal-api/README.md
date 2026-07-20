# <img src="https://images.mindcloud.co/apps/icons/trove_1775668010154.png" alt="Trove logo" width="28" height="28"> Trove: Universal API

Enrich transactions with merchant data and submit correction feedback

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trove/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trove.headline.com/
- **Vendor API docs:** https://trove.headline.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Enrich Sample Transaction](actions/enrich-sample-transaction.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trove/latest/actions/enrich-sample-transaction?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Bulk Transactions](actions/enrich-bulk-transactions.md) | POST | Creates a bulk transaction enrichment request in Trove. |
| [Enrich Sample Transaction](actions/enrich-sample-transaction.md) | GET | Retrieves enrichment details for a sample transaction from Trove. |
| [Get Bulk Transaction Result](actions/get-bulk-transaction-result.md) | GET | Retrieves the result of a bulk enrichment request from Trove. |
| [Submit Enrichment Feedback](actions/submit-enrichment-feedback.md) | PUT | Submits transaction enrichment feedback to Trove. |

