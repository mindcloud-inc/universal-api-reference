# <img src="https://images.mindcloud.co/apps/icons/favicon-1-1_1775158433348.png" alt="Windsor.ai logo" width="28" height="28"> Windsor.ai: Universal API

Access linked-account metadata and connector data from Windsor.ai's analytics ETL platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/windsorai/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://windsor.ai/
- **Vendor API docs:** https://windsor.ai/api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Co-User Linked Accounts](actions/list-co-user-linked-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/list-co-user-linked-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts For All Data Sources](actions/list-accounts-for-all-data-sources.md) | GET | Retrieves connected accounts across all Windsor.ai data sources. |
| [List Co-User Linked Accounts](actions/list-co-user-linked-accounts.md) | GET | Retrieves co-user linked accounts from Windsor.ai. |

### Connectors

| Action | Method | Description |
| --- | --- | --- |
| [List Connectors](actions/list-connectors.md) | GET | Retrieves available connectors from Windsor.ai. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves workspace custom fields from Windsor.ai. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Compare Multiple Platforms](actions/compare-multiple-platforms.md) | GET | Retrieves cross-platform connector data from Windsor.ai. |
| [Get Connector Data](actions/get-connector-data.md) | GET | Retrieves report data from one Windsor.ai connector. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Generate Authorization Link For A Single Data Source](actions/generate-authorization-link-for-a-single-data-source.md) | GET | Generates a Windsor.ai authorization link for one data source. |
| [Generate Authorization Link For Any Data Source](actions/generate-authorization-link-for-any-data-source.md) | GET | Generates a Windsor.ai authorization link for any data source. |

