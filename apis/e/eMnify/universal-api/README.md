# <img src="https://images.mindcloud.co/apps/icons/e-mnify_1774022542888.png" alt="EMnify logo" width="28" height="28"> EMnify: Universal API

Manage IoT connectivity, SIMs, endpoints, and service profiles

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eMnify/latest
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.emnify.com
- **Vendor API docs:** https://docs.emnify.com/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Endpoint Details](actions/get-endpoint-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-endpoint-details?connectionId=$CONNECTION_ID&authToken=Paste%20the%20auth_token%20from%20Retrieve%20Authentication%20Token&endpointId=18811970" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Application Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Application Token](actions/create-application-token.md) | POST | Creates a new application token in EMnify. |
| [List Application Tokens](actions/list-application-tokens.md) | GET | Retrieves a list of application tokens from EMnify. |
| [Update Application Token](actions/update-application-token.md) | PUT | Updates an existing application token in EMnify. |

### Authentication Token

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Authentication Token](actions/retrieve-authentication-token.md) | POST | Retrieves an authentication token from EMnify. |

### Data Quota

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Endpoint Data Quota Details](actions/retrieve-endpoint-data-quota-details.md) | GET | Retrieves endpoint data quota details from EMnify. |
| [Set Endpoint Data Quota](actions/set-endpoint-data-quota.md) | POST | Sets a new data quota for an endpoint in EMnify. |

### Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Endpoint](actions/create-endpoint.md) | POST | Creates a new endpoint in EMnify. |
| [Delete Endpoint](actions/delete-endpoint.md) | DELETE | Deletes an endpoint and its child entities from EMnify. |
| [Get Endpoint Details](actions/get-endpoint-details.md) | GET | Retrieves details for an endpoint from EMnify. |
| [List Endpoints](actions/list-endpoints.md) | GET | Retrieves a list of endpoints from EMnify. |
| [Update Endpoint](actions/update-endpoint.md) | PUT | Updates an existing endpoint in EMnify. |

### Endpoint Connectivity Information

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Endpoint Connectivity Information](actions/retrieve-endpoint-connectivity-information.md) | GET | Retrieves connectivity information for an endpoint from EMnify. |

### Endpoint Event

| Action | Method | Description |
| --- | --- | --- |
| [List Endpoint Events](actions/list-endpoint-events.md) | GET | Retrieves events for an endpoint from EMnify. |

### Endpoint Sms

| Action | Method | Description |
| --- | --- | --- |
| [List Endpoint SMS Messages](actions/list-endpoint-sms-messages.md) | GET | Retrieves SMS messages for an endpoint from EMnify. |

### Endpoint Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Endpoint Usage And Cost Statistics](actions/get-endpoint-usage-and-cost-statistics.md) | GET | Retrieves endpoint usage and cost statistics from EMnify. |

### Endpoint Status

| Action | Method | Description |
| --- | --- | --- |
| [List Endpoint Statuses](actions/list-endpoint-statuses.md) | GET | Retrieves available endpoint statuses from EMnify. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves a list of events from EMnify. |

### Event Type

| Action | Method | Description |
| --- | --- | --- |
| [List Event Types](actions/list-event-types.md) | GET | Retrieves available event types from EMnify. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get My Organization Details](actions/get-my-organization-details.md) | GET | Retrieves your organization details from EMnify. |

### Organization Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Monthly Organization Traffic And Cost Statistics](actions/get-monthly-organization-traffic-and-cost-statistics.md) | GET | Retrieves monthly organization traffic and cost statistics from EMnify. |

### Service Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Profile](actions/create-service-profile.md) | POST | Creates a new service profile in EMnify. |
| [List Service Profiles](actions/list-service-profiles.md) | GET | Retrieves a list of service profiles from EMnify. |
| [Retrieve Service Profile](actions/retrieve-service-profile.md) | GET | Retrieves a service profile from EMnify. |
| [Update Service Profile](actions/update-service-profile.md) | PUT | Updates an existing service profile in EMnify. |

### Sim

| Action | Method | Description |
| --- | --- | --- |
| [List SIMs](actions/list-sims.md) | GET | Retrieves a list of SIMs from EMnify. |

### Sim Status

| Action | Method | Description |
| --- | --- | --- |
| [List SIM Statuses](actions/list-sim-statuses.md) | GET | Retrieves available SIM statuses from EMnify. |

### Tariff Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Tariff Profile Details](actions/get-tariff-profile-details.md) | GET | Retrieves tariff profile details from EMnify. |
| [List Tariff Profiles](actions/list-tariff-profiles.md) | GET | Retrieves a list of tariff profiles from EMnify. |

