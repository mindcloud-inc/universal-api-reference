# <img src="https://images.mindcloud.co/apps/icons/peak-idx_1775502743110.png" alt="PeakIDX logo" width="28" height="28"> PeakIDX: Universal API

PeakIDX real-estate search and lead-management API covering search criteria, saved-search results, and lead synchronization for tenant websites.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/peakIDX/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.peakidx.com/
- **Vendor API docs:** https://docs.peakidx.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Search Criteria](actions/get-search-criteria.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/get-search-criteria?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List Search Results](actions/list-search-results.md) | GET | Retrieves listings for a saved search in PeakIDX. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Lead](actions/create-or-update-lead.md) | POST | Creates or updates a lead in PeakIDX. |
| [List New Leads](actions/list-new-leads.md) | GET | Retrieves new leads from PeakIDX since the last sync. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Criteria](actions/get-search-criteria.md) | GET | Retrieves configured search criteria from PeakIDX. |

