# <img src="https://images.mindcloud.co/apps/icons/idclcj-sf-at-1775068589300_1775068596166.png" alt="Satori Cyber logo" width="28" height="28"> Satori Cyber: Universal API

Security data access governance platform for managing data stores, access policies, datasets, and authorization analytics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/satoriCyber/latest
- **Category:** Content & Files / Storage
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://satoricyber.com
- **Vendor API docs:** https://app.satoricyber.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Datastores](actions/list-datastores.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/list-datastores?connectionId=$CONNECTION_ID&accountId=acc_123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Attributes](actions/get-account-attributes.md) | GET | Retrieves attributes for an account in Satori Cyber. |
| [List Account Environments](actions/list-account-environments.md) | GET | Retrieves environments for an account in Satori Cyber. |
| [List Account Roles](actions/list-account-roles.md) | GET | Retrieves roles for an account in Satori Cyber. |
| [List Service Account Roles](actions/list-service-account-roles.md) | GET | Retrieves roles for a service account in Satori Cyber. |
| [Search AWS Accounts](actions/search-aws-accounts.md) | GET | Finds AWS accounts in Satori Cyber. |

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert](actions/get-alert.md) | GET | Retrieves alert details from Satori Cyber. |
| [Search Alerts](actions/search-alerts.md) | GET | Finds alerts in Satori Cyber. |

### Authorization

| Action | Method | Description |
| --- | --- | --- |
| [Get Authorization Analytics Metrics](actions/get-authorization-analytics-metrics.md) | GET | Retrieves authorization analytics metrics from Satori Cyber. |
| [Search Authorization Analytics](actions/search-authorization-analytics.md) | GET | Finds authorization analytics records in Satori Cyber. |

### Cluster

| Action | Method | Description |
| --- | --- | --- |
| [Search Atlas Clusters](actions/search-atlas-clusters.md) | GET | Finds Atlas clusters in Satori Cyber. |

### Data

| Action | Method | Description |
| --- | --- | --- |
| [List Data Access Rule History](actions/list-data-access-rule-history.md) | GET | Retrieves data access rule history from Satori Cyber. |
| [List Data Access Rules Overview](actions/list-data-access-rules-overview.md) | GET | Retrieves data access rule overviews from Satori Cyber. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset Access Details](actions/get-dataset-access-details.md) | GET | Retrieves dataset access details from Satori Cyber. |
| [Get Dataset Connection Details](actions/get-dataset-connection-details.md) | GET | Retrieves dataset connection details from Satori Cyber. |
| [Get Datastore State](actions/get-datastore-state.md) | GET | Retrieves the state of a datastore in Satori Cyber. |
| [Search Datasets](actions/search-datasets.md) | GET | Finds datasets in Satori Cyber. |

### Datastore

| Action | Method | Description |
| --- | --- | --- |
| [Get Discovered Datastore Count](actions/get-discovered-datastore-count.md) | GET | Retrieves the discovered datastore count from Satori Cyber. |
| [List Datastores](actions/list-datastores.md) | GET | Retrieves datastore records from Satori Cyber. |

### Directory

| Action | Method | Description |
| --- | --- | --- |
| [List Directory Groups](actions/list-directory-groups.md) | GET | Retrieves directory groups from Satori Cyber. |
| [Search Directory Group Suggestions](actions/search-directory-group-suggestions.md) | GET | Finds directory group suggestions in Satori Cyber. |
| [Search Directory Member Suggestions](actions/search-directory-member-suggestions.md) | GET | Finds directory member suggestions in Satori Cyber. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Search GCP Projects](actions/search-gcp-projects.md) | GET | Finds GCP projects in Satori Cyber. |

### Security

| Action | Method | Description |
| --- | --- | --- |
| [Get Security Policy Statistics](actions/get-security-policy-statistics.md) | GET | Retrieves security policy statistics from Satori Cyber. |

### Taxonomy

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Taxonomy](actions/list-custom-taxonomy.md) | GET | Retrieves custom taxonomy terms from Satori Cyber. |
| [List Satori Taxonomy](actions/list-satori-taxonomy.md) | GET | Retrieves Satori taxonomy terms from Satori Cyber. |

