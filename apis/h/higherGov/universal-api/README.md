# <img src="https://images.mindcloud.co/apps/icons/higher-gov_1778005600533.png" alt="HigherGov logo" width="28" height="28"> HigherGov: Universal API

Access HigherGov government market intelligence data, including opportunities, contract and grant awards, awardees, agencies, documents, people, pursuits, and reference data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/higherGov/latest
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.highergov.com/
- **Vendor API docs:** https://docs.highergov.com/import-and-export/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agencies](actions/list-agencies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-agencies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Agency

| Action | Method | Description |
| --- | --- | --- |
| [List Agencies](actions/list-agencies.md) | GET | Retrieves agencies from HigherGov. |

### Awardee

| Action | Method | Description |
| --- | --- | --- |
| [List Awardees](actions/list-awardees.md) | GET | Retrieves awardees from HigherGov. |

### Awardee Partnership

| Action | Method | Description |
| --- | --- | --- |
| [List Awardee Partnerships](actions/list-awardee-partnerships.md) | GET | Retrieves awardee partnerships from HigherGov. |

### Contract Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [List Contract Vehicles](actions/list-contract-vehicles.md) | GET | Retrieves contract vehicles from HigherGov. |

### Federal Contract

| Action | Method | Description |
| --- | --- | --- |
| [List Federal Contracts](actions/list-federal-contracts.md) | GET | Retrieves federal contract awards from HigherGov. |

### Federal Grant

| Action | Method | Description |
| --- | --- | --- |
| [List Federal Grants](actions/list-federal-grants.md) | GET | Retrieves federal grant awards from HigherGov. |

### Grant Program

| Action | Method | Description |
| --- | --- | --- |
| [List Grant Programs](actions/list-grant-programs.md) | GET | Retrieves grant programs from HigherGov. |

### Idv Award

| Action | Method | Description |
| --- | --- | --- |
| [List IDV Awards](actions/list-idv-awards.md) | GET | Retrieves federal IDV awards from HigherGov. |

### Mentor Protege Relationship

| Action | Method | Description |
| --- | --- | --- |
| [List Mentor Protege Relationships](actions/list-mentor-protege-relationships.md) | GET | Retrieves mentor-protege relationships from HigherGov. |

### Naics Code

| Action | Method | Description |
| --- | --- | --- |
| [List NAICS Codes](actions/list-naics-codes.md) | GET | Retrieves NAICS codes from HigherGov. |

### National Stock Number

| Action | Method | Description |
| --- | --- | --- |
| [List NSNs](actions/list-nsns.md) | GET | Retrieves national stock numbers from HigherGov. |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [List Opportunities](actions/list-opportunities.md) | GET | Retrieves government opportunities from HigherGov. |

### Opportunity Document

| Action | Method | Description |
| --- | --- | --- |
| [List Opportunity Documents](actions/list-opportunity-documents.md) | GET | Retrieves opportunity documents from HigherGov. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [List People](actions/list-people.md) | GET | Retrieves people from HigherGov. |

### Psc Code

| Action | Method | Description |
| --- | --- | --- |
| [List PSC Codes](actions/list-psc-codes.md) | GET | Retrieves PSC codes from HigherGov. |

### Pursuit

| Action | Method | Description |
| --- | --- | --- |
| [List Pursuits](actions/list-pursuits.md) | GET | Retrieves authenticated pursuits from HigherGov. |

### State And Local Contract

| Action | Method | Description |
| --- | --- | --- |
| [List State And Local Contracts](actions/list-state-and-local-contracts.md) | GET | Retrieves state and local contract awards from HigherGov. |

### Subcontract

| Action | Method | Description |
| --- | --- | --- |
| [List Subcontracts](actions/list-subcontracts.md) | GET | Retrieves subcontract awards from HigherGov. |

### Subgrant

| Action | Method | Description |
| --- | --- | --- |
| [List Subgrants](actions/list-subgrants.md) | GET | Retrieves subgrant awards from HigherGov. |

