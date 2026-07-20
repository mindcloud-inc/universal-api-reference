# <img src="https://images.mindcloud.co/apps/icons/cpsc-icon_1777488775398.jpeg" alt="CPSC Recalls Retrieval logo" width="28" height="28"> CPSC Recalls Retrieval: Universal API

Retrieve publicly available recall records from the U.S. Consumer Product Safety Commission recall database via the official CPSC Recall Retrieval REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cPSCRecallsRetrieval/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cpsc.gov/Recalls/CPSC-Recalls-Application-Program-Interface-API-Information?language=en
- **Vendor API docs:** https://www.cpsc.gov/Recalls/CPSC-Recalls-Application-Program-Interface-API-Information?language=en

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Recalls](actions/search-recalls.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cPSCRecallsRetrieval/latest/actions/search-recalls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Recall

| Action | Method | Description |
| --- | --- | --- |
| [Search Recalls](actions/search-recalls.md) | GET | Finds public product recalls in CPSC by search fields. |

