# <img src="https://images.mindcloud.co/apps/icons/new-relic_1775055670917.png" alt="New Relic logo" width="28" height="28"> New Relic: Universal API

Monitor New Relic applications, alerts, deployments, browser apps, key transactions, and telemetry metrics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/newRelic/latest
- **Category:** IT Operations / Observability
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://newrelic.com/
- **Vendor API docs:** https://docs.newrelic.com/docs/apis/rest-api-v2/get-started/introduction-new-relic-rest-api-v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Applications](actions/list-applications.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Alert Condition

| Action | Method | Description |
| --- | --- | --- |
| [Create Alert Condition](actions/create-alert-condition.md) | POST | Creates a new alert condition in New Relic. |
| [Delete Alert Condition](actions/delete-alert-condition.md) | DELETE | Deletes an existing alert condition from New Relic. |
| [List Alert Conditions](actions/list-alert-conditions.md) | GET | Retrieves alert conditions from New Relic. |
| [Update Alert Condition](actions/update-alert-condition.md) | PUT | Updates an existing alert condition in New Relic. |

### Alert Condition Entity

| Action | Method | Description |
| --- | --- | --- |
| [Add Entity To Alert Condition](actions/add-entity-to-alert-condition.md) | PUT | Adds an entity to an alert condition in New Relic. |
| [Remove Entity From Alert Condition](actions/remove-entity-from-alert-condition.md) | DELETE | Removes an entity from an alert condition in New Relic. |

### Alert Policy

| Action | Method | Description |
| --- | --- | --- |
| [Create Alert Policy](actions/create-alert-policy.md) | POST | Creates a new alert policy in New Relic. |
| [Delete Alert Policy](actions/delete-alert-policy.md) | DELETE | Deletes an existing alert policy from New Relic. |
| [List Alert Policies](actions/list-alert-policies.md) | GET | Retrieves alert policies from New Relic. |
| [Update Alert Policy](actions/update-alert-policy.md) | PUT | Updates an existing alert policy in New Relic. |

### Application Metric

| Action | Method | Description |
| --- | --- | --- |
| [List Application Metrics](actions/list-application-metrics.md) | GET | Retrieves application metrics from New Relic. |

### Application Metric Timeslice

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Metric Timeslice Data](actions/get-application-metric-timeslice-data.md) | GET | Retrieves application metric timeslice data from New Relic. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Change Application Alias](actions/change-application-alias.md) | PUT | Updates an application alias in New Relic. |
| [Get Application Details](actions/get-application-details.md) | GET | Retrieves application details from New Relic. |
| [List Applications](actions/list-applications.md) | GET | Retrieves applications from New Relic. |

### Browser Application

| Action | Method | Description |
| --- | --- | --- |
| [Create Browser Application](actions/create-browser-application.md) | POST | Creates a new browser application in New Relic. |
| [List Browser Applications](actions/list-browser-applications.md) | GET | Retrieves browser applications from New Relic. |

### Deployments

| Action | Method | Description |
| --- | --- | --- |
| [List Deployments](actions/list-deployments.md) | GET | Retrieves deployments from New Relic. |
| [Record Deployment](actions/record-deployment.md) | POST | Records a deployment in New Relic. |

### External Service Condition

| Action | Method | Description |
| --- | --- | --- |
| [Create External Service Condition](actions/create-external-service-condition.md) | POST | Creates a new external service condition in New Relic. |
| [Delete External Service Condition](actions/delete-external-service-condition.md) | DELETE | Deletes an existing external service condition from New Relic. |
| [List External Service Conditions](actions/list-external-service-conditions.md) | GET | Retrieves external service conditions from New Relic. |
| [Update External Service Condition](actions/update-external-service-condition.md) | PUT | Updates an existing external service condition in New Relic. |

### Key Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Key Transaction](actions/get-key-transaction.md) | GET | Retrieves a key transaction from New Relic. |
| [List Key Transactions](actions/list-key-transactions.md) | GET | Retrieves key transactions from New Relic. |

### Multi-location Synthetics Condition

| Action | Method | Description |
| --- | --- | --- |
| [Create Multi-Location Synthetics Condition](actions/create-multi-location-synthetics-condition.md) | POST | Creates a new multi-location synthetics condition in New Relic. |
| [Delete Multi-Location Synthetics Condition](actions/delete-multi-location-synthetics-condition.md) | DELETE | Deletes an existing multi-location synthetics condition from New Relic. |
| [List Multi-Location Synthetics Conditions](actions/list-multi-location-synthetics-conditions.md) | GET | Retrieves multi-location synthetics conditions from New Relic. |
| [Update Multi-Location Synthetics Condition](actions/update-multi-location-synthetics-condition.md) | PUT | Updates an existing multi-location synthetics condition in New Relic. |

### Nrql Condition

| Action | Method | Description |
| --- | --- | --- |
| [Create NRQL Condition](actions/create-nrql-condition.md) | POST | Creates a new NRQL condition in New Relic. |
| [Delete NRQL Condition](actions/delete-nrql-condition.md) | DELETE | Deletes an existing NRQL condition from New Relic. |
| [List NRQL Conditions](actions/list-nrql-conditions.md) | GET | Retrieves NRQL conditions from New Relic. |
| [Update NRQL Condition](actions/update-nrql-condition.md) | PUT | Updates an existing NRQL condition in New Relic. |

### Synthetics Condition

| Action | Method | Description |
| --- | --- | --- |
| [Create Synthetics Condition](actions/create-synthetics-condition.md) | POST | Creates a new synthetics condition in New Relic. |
| [Delete Synthetics Condition](actions/delete-synthetics-condition.md) | DELETE | Deletes an existing synthetics condition from New Relic. |
| [List Synthetics Conditions](actions/list-synthetics-conditions.md) | GET | Retrieves synthetics conditions from New Relic. |
| [Update Synthetics Condition](actions/update-synthetics-condition.md) | PUT | Updates an existing synthetics condition in New Relic. |

