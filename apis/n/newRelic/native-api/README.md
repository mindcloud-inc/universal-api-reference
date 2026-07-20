# New Relic: Native API Reference

A consolidated summary of New Relic's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://docs.newrelic.com/docs/apis/rest-api-v2/get-started/introduction-new-relic-rest-api-v2/
- **API base URL:** `https://api.newrelic.com/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.newrelic.com/docs/apis/rest-api-v2/get-started/introduction-new-relic-rest-api-v2/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Entity To Alert Condition](actions/add-entity-to-alert-condition.md) | `PUT /alerts_entity_conditions/:entityId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Change Application Alias](actions/change-application-alias.md) | `PUT /applications/:appId.json` | [docs](https://docs.newrelic.com/docs/apis/rest-api-v2/application-examples-v2/change-alias-your-application-v2/) |
| [Create Alert Condition](actions/create-alert-condition.md) | `POST /alerts_conditions/policies/:policyId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Create Alert Policy](actions/create-alert-policy.md) | `POST /alerts_policies.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Create Browser Application](actions/create-browser-application.md) | `POST /browser_applications.json` | [docs](https://docs.newrelic.com/docs/apis/rest-api-v2/browser-examples-v2/add-or-list-browser-apps-api-v2/) |
| [Create External Service Condition](actions/create-external-service-condition.md) | `POST /alerts_external_service_conditions/policies/:policyId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Create Multi-Location Synthetics Condition](actions/create-multi-location-synthetics-condition.md) | `POST /alerts_location_failure_conditions/policies/:policyId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Create NRQL Condition](actions/create-nrql-condition.md) | `POST /alerts_nrql_conditions/policies/:policyId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Create Synthetics Condition](actions/create-synthetics-condition.md) | `POST /alerts_synthetics_conditions/policies/:policyId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Delete Alert Condition](actions/delete-alert-condition.md) | `DELETE /alerts_conditions/:conditionId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Delete Alert Policy](actions/delete-alert-policy.md) | `DELETE /alerts_policies/:policyId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Delete External Service Condition](actions/delete-external-service-condition.md) | `DELETE /alerts_external_service_conditions/:conditionId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Delete Multi-Location Synthetics Condition](actions/delete-multi-location-synthetics-condition.md) | `DELETE /alerts_location_failure_conditions/:conditionId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Delete NRQL Condition](actions/delete-nrql-condition.md) | `DELETE /alerts_nrql_conditions/:conditionId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Delete Synthetics Condition](actions/delete-synthetics-condition.md) | `DELETE /alerts_synthetics_conditions/:conditionId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Get Application Details](actions/get-application-details.md) | `GET /applications/:appId.json` | [docs](https://docs.newrelic.com/docs/apis/rest-api-v2/application-examples-v2/summary-data-examples-v2/) |
| [Get Application Metric Timeslice Data](actions/get-application-metric-timeslice-data.md) | `GET /applications/:appId/metrics/data.json` | [docs](https://docs.newrelic.com/docs/apis/rest-api-v2/application-examples-v2/list-your-app-id-metric-timeslice-data-v2/) |
| [Get Key Transaction](actions/get-key-transaction.md) | `GET /key_transactions/:keyTransactionId.json` | [docs](https://docs.newrelic.com/docs/apis/rest-api-v2/application-examples-v2/summary-data-examples-v2/) |
| [List Alert Conditions](actions/list-alert-conditions.md) | `GET /alerts_conditions.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [List Alert Policies](actions/list-alert-policies.md) | `GET /alerts_policies.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [List Application Metrics](actions/list-application-metrics.md) | `GET /applications/:appId/metrics.json` | [docs](https://docs.newrelic.com/docs/apis/rest-api-v2/application-examples-v2/list-your-app-id-metric-timeslice-data-v2/) |
| [List Applications](actions/list-applications.md) | `GET /applications.json` | [docs](https://docs.newrelic.com/docs/apis/rest-api-v2/application-examples-v2/list-your-app-id-metric-timeslice-data-v2/) |
| [List Browser Applications](actions/list-browser-applications.md) | `GET /browser_applications.json` | [docs](https://docs.newrelic.com/docs/apis/rest-api-v2/browser-examples-v2/add-or-list-browser-apps-api-v2/) |
| [List Deployments](actions/list-deployments.md) | `GET /applications/:appId/deployments.json` | [docs](https://docs.newrelic.com/docs/apm/apm-ui-pages/events/record-deployments/) |
| [List External Service Conditions](actions/list-external-service-conditions.md) | `GET /alerts_external_service_conditions.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [List Key Transactions](actions/list-key-transactions.md) | `GET /key_transactions.json` | [docs](https://docs.newrelic.com/docs/apis/rest-api-v2/application-examples-v2/summary-data-examples-v2/) |
| [List Multi-Location Synthetics Conditions](actions/list-multi-location-synthetics-conditions.md) | `GET /alerts_location_failure_conditions/policies/:policyId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [List NRQL Conditions](actions/list-nrql-conditions.md) | `GET /alerts_nrql_conditions.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [List Synthetics Conditions](actions/list-synthetics-conditions.md) | `GET /alerts_synthetics_conditions.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Record Deployment](actions/record-deployment.md) | `POST /applications/:appId/deployments.json` | [docs](https://docs.newrelic.com/docs/apm/apm-ui-pages/events/record-deployments/) |
| [Remove Entity From Alert Condition](actions/remove-entity-from-alert-condition.md) | `DELETE /alerts_entity_conditions/:entityId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Update Alert Condition](actions/update-alert-condition.md) | `PUT /alerts_conditions/:conditionId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Update Alert Policy](actions/update-alert-policy.md) | `PUT /alerts_policies/:policyId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Update External Service Condition](actions/update-external-service-condition.md) | `PUT /alerts_external_service_conditions/:conditionId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Update Multi-Location Synthetics Condition](actions/update-multi-location-synthetics-condition.md) | `PUT /alerts_location_failure_conditions/:conditionId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Update NRQL Condition](actions/update-nrql-condition.md) | `PUT /alerts_nrql_conditions/:conditionId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
| [Update Synthetics Condition](actions/update-synthetics-condition.md) | `PUT /alerts_synthetics_conditions/:conditionId.json` | [docs](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/) |
