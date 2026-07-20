# <img src="https://images.mindcloud.co/apps/icons/solace-pub-sub_1776770908607.png" alt="Solace PubSub+ logo" width="28" height="28"> Solace PubSub+: Universal API

Solace PubSub+ Cloud provides managed event broker services, Event Portal resources, platform administration, API tokens, billing usage, and related Solace Cloud operations through REST APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/solacePubSub/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://solace.com/products/platform/cloud/
- **Vendor API docs:** https://api.solace.dev/cloud/reference/using-the-v2-rest-apis-for-pubsub-cloud

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Tokens](actions/get-api-tokens.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-api-tokens?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Api Token

| Action | Method | Description |
| --- | --- | --- |
| [Get API Token](actions/get-api-token.md) | GET | Retrieves an API token from Solace PubSub+. |
| [Get API Tokens](actions/get-api-tokens.md) | GET | Retrieves API tokens from Solace PubSub+. |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Application](actions/get-application.md) | GET | Retrieves an application from Solace PubSub+. |
| [Get Applications](actions/get-applications.md) | GET | Retrieves applications from Solace PubSub+. |

### Application Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Domain](actions/get-application-domain.md) | GET | Retrieves an application domain from Solace PubSub+. |
| [Get Application Domains](actions/get-application-domains.md) | GET | Retrieves application domains from Solace PubSub+. |

### Broker Service Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Broker Service Versions](actions/get-broker-service-versions.md) | GET | Retrieves broker service versions from Solace PubSub+. |

### Broker State

| Action | Method | Description |
| --- | --- | --- |
| [Get Broker State](actions/get-broker-state.md) | GET | Retrieves broker state from Solace PubSub+. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Contacts](actions/get-organization-contacts.md) | GET | Retrieves organization contacts from Solace PubSub+. |

### Datacenter

| Action | Method | Description |
| --- | --- | --- |
| [Get Datacenter](actions/get-datacenter.md) | GET | Retrieves a datacenter from Solace PubSub+. |
| [Get Datacenters](actions/get-datacenters.md) | GET | Retrieves datacenters from Solace PubSub+. |

### Default Broker Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Broker Versions](actions/get-default-broker-versions.md) | GET | Retrieves default broker versions from Solace PubSub+. |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Get Platform Environment](actions/get-platform-environment.md) | GET | Retrieves a platform environment from Solace PubSub+. |
| [Get Platform Environments](actions/get-platform-environments.md) | GET | Retrieves platform environments from Solace PubSub+. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Events](actions/get-events.md) | GET | Retrieves events from Solace PubSub+. |

### Event Broker Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Broker Service](actions/get-event-broker-service.md) | GET | Retrieves an event broker service from Solace PubSub+. |
| [Get Event Broker Services](actions/get-event-broker-services.md) | GET | Retrieves event broker services from Solace PubSub+. |

### Maintenance Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Maintenance Activities](actions/get-maintenance-activities.md) | GET | Retrieves maintenance activities from Solace PubSub+. |
| [Get Maintenance Activity](actions/get-maintenance-activity.md) | GET | Retrieves a maintenance activity from Solace PubSub+. |

### Maintenance Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get Maintenance Schedule](actions/get-maintenance-schedule.md) | GET | Retrieves a maintenance schedule from Solace PubSub+. |
| [Get Maintenance Schedules](actions/get-maintenance-schedules.md) | GET | Retrieves maintenance schedules from Solace PubSub+. |

### Resource Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Assignments](actions/get-resource-assignments.md) | GET | Retrieves resource assignments from Solace PubSub+. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Get Roles](actions/get-roles.md) | GET | Retrieves roles from Solace PubSub+. |

### Service Class

| Action | Method | Description |
| --- | --- | --- |
| [Get Service Class](actions/get-service-class.md) | GET | Retrieves a service class from Solace PubSub+. |
| [Get Service Classes](actions/get-service-classes.md) | GET | Retrieves service classes from Solace PubSub+. |

### Service Operation

| Action | Method | Description |
| --- | --- | --- |
| [Get Service Operation](actions/get-service-operation.md) | GET | Retrieves a service operation from Solace PubSub+. |
| [Get Service Operations](actions/get-service-operations.md) | GET | Retrieves service operations from Solace PubSub+. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Users](actions/get-users.md) | GET | Retrieves users from Solace PubSub+. |

### User Group

| Action | Method | Description |
| --- | --- | --- |
| [Get User Group](actions/get-user-group.md) | GET | Retrieves a user group from Solace PubSub+. |
| [Get User Groups](actions/get-user-groups.md) | GET | Retrieves user groups from Solace PubSub+. |

