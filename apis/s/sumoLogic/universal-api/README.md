# <img src="https://images.mindcloud.co/apps/icons/sumo-logic_1776783205351.png" alt="Sumo Logic logo" width="28" height="28"> Sumo Logic: Universal API

Sumo Logic provides cloud-native log management, analytics, monitoring, and security intelligence APIs for working with users, roles, monitors, searches, fields, ingestion, and account configuration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sumoLogic/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sumologic.com/
- **Vendor API docs:** https://www.sumologic.com/help/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [List Tokens](actions/list-tokens.md) | GET | Retrieves tokens from your Sumo Logic token library. |

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [List Access Keys](actions/list-access-keys.md) | GET | Retrieves access keys from your Sumo Logic account. |
| [List Personal Access Keys](actions/list-personal-access-keys.md) | GET | Retrieves access keys owned by your Sumo Logic user. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [List Apps](actions/list-apps.md) | GET | Retrieves apps from the Sumo Logic App Catalog. |
| [List Apps V2](actions/list-apps-v2.md) | GET | Retrieves apps from the Sumo Logic App Catalog. |

### Budgets

| Action | Method | Description |
| --- | --- | --- |
| [List Ingest Budgets](actions/list-ingest-budgets.md) | GET | Retrieves ingest budgets from your Sumo Logic organization. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [List Connections](actions/list-connections.md) | GET | Retrieves connections from your Sumo Logic organization. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Built-In Fields](actions/list-built-in-fields.md) | GET | Retrieves built-in fields from your Sumo Logic account. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from your Sumo Logic account. |
| [List Dropped Fields](actions/list-dropped-fields.md) | GET | Retrieves dropped fields from your Sumo Logic account. |

### Data Forwarding Rule

| Action | Method | Description |
| --- | --- | --- |
| [List Log Data Forwarding Rules](actions/list-log-data-forwarding-rules.md) | GET | Retrieves S3 data forwarding rules from Sumo Logic. |

### Dynamic Parsing Rule

| Action | Method | Description |
| --- | --- | --- |
| [List Dynamic Parsing Rules](actions/list-dynamic-parsing-rules.md) | GET | Retrieves dynamic parsing rules from your Sumo Logic organization. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Health Events](actions/list-health-events.md) | GET | Retrieves unresolved health events from your Sumo Logic account. |

### Field Extraction Rule

| Action | Method | Description |
| --- | --- | --- |
| [List Field Extraction Rules](actions/list-field-extraction-rules.md) | GET | Retrieves field extraction rules from your Sumo Logic organization. |

### Partition

| Action | Method | Description |
| --- | --- | --- |
| [List Partitions](actions/list-partitions.md) | GET | Retrieves partitions from your Sumo Logic organization. |

### Policies

| Action | Method | Description |
| --- | --- | --- |
| [List Data Deletion Rules](actions/list-data-deletion-rules.md) | GET | Retrieves data deletion rules from your Sumo Logic organization. |
| [List Data Masking Rules](actions/list-data-masking-rules.md) | GET | Retrieves data masking rules from your Sumo Logic organization. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [List Log Searches](actions/list-log-searches.md) | GET | Retrieves saved log searches from Sumo Logic. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from your Sumo Logic organization. |
| [List Roles V2](actions/list-roles-v2.md) | GET | Retrieves roles from your Sumo Logic organization. |

### Service Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Service Accounts](actions/list-service-accounts.md) | GET | Retrieves service accounts from your Sumo Logic organization. |

### Transformation Rule

| Action | Method | Description |
| --- | --- | --- |
| [List Transformation Rules](actions/list-transformation-rules.md) | GET | Retrieves transformation rules from your Sumo Logic organization. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from your Sumo Logic organization. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [List Scheduled Views](actions/list-scheduled-views.md) | GET | Retrieves scheduled views from your Sumo Logic organization. |

