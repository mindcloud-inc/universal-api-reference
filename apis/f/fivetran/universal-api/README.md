# <img src="https://images.mindcloud.co/apps/icons/fivetran_1776256403572.png" alt="Fivetran logo" width="28" height="28"> Fivetran: Universal API

Fivetran is a managed data movement platform for programmatically managing accounts, destinations, connections, schemas, transformations, webhooks, and operational sync workflows through the Fivetran REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fivetran/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fivetran.com/
- **Vendor API docs:** https://fivetran.com/docs/rest-api/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create Connect Card](actions/create-connect-card.md) | POST | Creates a Connect Card for a connection in Fivetran. |

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [Get Source Table Columns Config](actions/get-source-table-columns-config.md) | GET | Retrieves source table column configuration from Fivetran. |
| [Update Connection Column Config](actions/update-connection-column-config.md) | PUT | Updates column configuration for a connection schema in Fivetran. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Create Connection](actions/create-connection.md) | POST | Creates a new connection in your Fivetran account. |
| [Get Connection](actions/get-connection.md) | GET | Retrieves a connection from your Fivetran account. |
| [List Connections](actions/list-connections.md) | GET | Retrieves connections from your Fivetran account. |
| [List Group Connections](actions/list-group-connections.md) | GET | Retrieves connections for a group in Fivetran. |
| [Re-sync Connection](actions/resync-connection.md) | PUT | Starts a re-sync for a connection in Fivetran. |
| [Run Connection Setup Tests](actions/run-connection-setup-tests.md) | PUT | Runs setup tests for a connection in Fivetran. |
| [Sync Connection](actions/sync-connection.md) | PUT | Starts a sync for a connection in Fivetran. |
| [Update Connection](actions/update-connection.md) | PUT | Updates an existing connection in your Fivetran account. |

### Connectors

| Action | Method | Description |
| --- | --- | --- |
| [Get Connector Type Metadata](actions/get-connector-type-metadata.md) | GET | Retrieves metadata for a connector type in Fivetran. |
| [List Connector Types](actions/list-connector-types.md) | GET | Retrieves available connector types from Fivetran. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Get Connection Schema Config](actions/get-connection-schema-config.md) | GET | Retrieves schema configuration for a connection in Fivetran. |
| [Reload Connection Schema Config](actions/reload-connection-schema-config.md) | PUT | Reloads schema configuration for a connection in Fivetran. |
| [Re-sync Connection Table Data](actions/resync-connection-table-data.md) | PUT | Re-syncs table data for a connection in Fivetran. |
| [Set Up Connection Schema Config](actions/set-up-connection-schema-config.md) | POST | Creates schema configuration for a connection in Fivetran. |
| [Update Connection Schema Config](actions/update-connection-schema-config.md) | PUT | Updates schema configuration for a connection in Fivetran. |
| [Update Connection Table Config](actions/update-connection-table-config.md) | PUT | Updates table configuration for a connection schema in Fivetran. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in your Fivetran account. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from your Fivetran account. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from your Fivetran account. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in your Fivetran account. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Transformation Project](actions/get-transformation-project.md) | GET | Retrieves a transformation project from your Fivetran account. |
| [List Transformation Projects](actions/list-transformation-projects.md) | GET | Retrieves transformation projects from your Fivetran account. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Public SSH Key](actions/get-group-public-ssh-key.md) | GET | Retrieves a group's public SSH key from Fivetran. |

### Sync States

| Action | Method | Description |
| --- | --- | --- |
| [Get Connection State](actions/get-connection-state.md) | GET | Retrieves sync state for a connection in Fivetran. |
| [Update Connection State](actions/update-connection-state.md) | PUT | Updates sync state for a connection in Fivetran. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves account details for your Fivetran account. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Group Users](actions/list-group-users.md) | GET | Retrieves users for a group in Fivetran. |

### Warehouses

| Action | Method | Description |
| --- | --- | --- |
| [Create Destination](actions/create-destination.md) | POST | Creates a new destination in your Fivetran account. |
| [Get Destination](actions/get-destination.md) | GET | Retrieves a destination from your Fivetran account. |
| [List Destinations](actions/list-destinations.md) | GET | Retrieves destinations from your Fivetran account. |
| [Run Destination Setup Tests](actions/run-destination-setup-tests.md) | PUT | Runs setup tests for a destination in Fivetran. |
| [Update Destination](actions/update-destination.md) | PUT | Updates an existing destination in your Fivetran account. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from your Fivetran account. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from your Fivetran account. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Get Transformation](actions/get-transformation.md) | GET | Retrieves a transformation from your Fivetran account. |
| [List Transformations](actions/list-transformations.md) | GET | Retrieves transformations from your Fivetran account. |
| [Run Transformation](actions/run-transformation.md) | PUT | Runs a transformation in your Fivetran account. |

