# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-05-01-as-10_1777643408063.png" alt="openFDA Drug logo" width="28" height="28"> openFDA Drug: Universal API

Public FDA drug datasets exposed through the official openFDA Drug API, including adverse events, structured product labeling, NDC directory records, recall enforcement reports, Drugs@FDA approvals, and drug shortages.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openFDADrug/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://open.fda.gov/apis/drug/
- **Vendor API docs:** https://open.fda.gov/apis/drug/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Count Drug Adverse Event Records](actions/count-drug-adverse-event-records.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFDADrug/latest/actions/count-drug-adverse-event-records?connectionId=$CONNECTION_ID&count=patient.drug.medicinalproduct.exact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Drug Adverse Event Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Drug Adverse Event Records](actions/count-drug-adverse-event-records.md) | GET | Counts drug adverse event records in openFDA Drug by field. |

### Drug Adverse Event Record

| Action | Method | Description |
| --- | --- | --- |
| [Search Drug Adverse Event Records](actions/search-drug-adverse-event-records.md) | GET | Finds drug adverse event records in openFDA Drug. |

### Drug Enforcement Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Drug Enforcement Records](actions/count-drug-enforcement-records.md) | GET | Counts drug recall enforcement records in openFDA Drug by field. |

### Drug Enforcement Record

| Action | Method | Description |
| --- | --- | --- |
| [Search Drug Enforcement Records](actions/search-drug-enforcement-records.md) | GET | Finds drug recall enforcement records in openFDA Drug. |

### Drug Label Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Drug Label Records](actions/count-drug-label-records.md) | GET | Counts drug label records in openFDA Drug by field. |

### Drug Label Record

| Action | Method | Description |
| --- | --- | --- |
| [Search Drug Label Records](actions/search-drug-label-records.md) | GET | Finds drug label records in openFDA Drug. |

### Drug Ndc Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Drug NDC Records](actions/count-drug-ndc-records.md) | GET | Counts drug NDC records in openFDA Drug by field. |

### Drug Ndc Record

| Action | Method | Description |
| --- | --- | --- |
| [Search Drug NDC Records](actions/search-drug-ndc-records.md) | GET | Finds drug NDC records in openFDA Drug. |

### Drug Shortage Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Drug Shortage Records](actions/count-drug-shortage-records.md) | GET | Counts drug shortage records in openFDA Drug by field. |

### Drug Shortage Record

| Action | Method | Description |
| --- | --- | --- |
| [Search Drug Shortage Records](actions/search-drug-shortage-records.md) | GET | Finds drug shortage records in openFDA Drug. |

### Drugs@fda Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Drugs@FDA Records](actions/count-drugs-fda-records.md) | GET | Counts Drugs@FDA records in openFDA Drug by field. |

### Drugs@fda Record

| Action | Method | Description |
| --- | --- | --- |
| [Search Drugs@FDA Records](actions/search-drugs-fda-records.md) | GET | Finds Drugs@FDA records in openFDA Drug. |

