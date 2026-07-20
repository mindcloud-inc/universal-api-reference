# <img src="https://images.mindcloud.co/apps/icons/images-14_1775842884782.png" alt="MQTT logo" width="28" height="28"> MQTT: Universal API

Manage HiveMQ Cloud MQTT credentials, permissions, roles, clients, and cluster authentication settings through the HiveMQ Cloud REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mQTT/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hivemq.com/products-platforms/cloud/
- **Vendor API docs:** https://docs.hivemq.com/hivemq-cloud/rest-api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List MQTT Roles](actions/list-mqtt-roles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-mqtt-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Broker Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Broker Metrics](actions/get-broker-metrics.md) | GET | Retrieves broker metrics from HiveMQ Cloud. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Certificate](actions/get-client-certificate.md) | GET |  |
| [Get Client JWT Config](actions/get-client-jwt-config.md) | GET |  |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Disconnect MQTT Client](actions/disconnect-mqtt-client.md) | DELETE | Disconnects an MQTT client from HiveMQ Cloud. |
| [Invalidate MQTT Client Session](actions/invalidate-mqtt-client-session.md) | DELETE | Invalidates an MQTT client session in HiveMQ Cloud. |
| [Search MQTT Clients](actions/search-mqtt-clients.md) | GET | Finds MQTT clients in HiveMQ Cloud by query parameters. |

### Mqtt Client

| Action | Method | Description |
| --- | --- | --- |
| [Get MQTT Client](actions/get-mqtt-client.md) | GET | Retrieves MQTT client details from HiveMQ Cloud. |
| [Get MQTT Client Connection State](actions/get-mqtt-client-connection-state.md) | GET | Retrieves an MQTT client's connection state from HiveMQ Cloud. |
| [List MQTT Client Subscriptions](actions/list-mqtt-client-subscriptions.md) | GET | Retrieves subscriptions for an MQTT client in HiveMQ Cloud. |
| [List MQTT Clients](actions/list-mqtt-clients.md) | GET | Retrieves MQTT clients from HiveMQ Cloud. |

### Mqtt Credential

| Action | Method | Description |
| --- | --- | --- |
| [Attach Role To Credential](actions/attach-role-to-credential.md) | PUT | Updates an MQTT credential in HiveMQ Cloud by attaching a role. |
| [Create MQTT Credential](actions/create-mqtt-credential.md) | POST | Creates a new MQTT credential in HiveMQ Cloud. |
| [Delete MQTT Credential](actions/delete-mqtt-credential.md) | DELETE | Deletes an MQTT credential from HiveMQ Cloud by username. |
| [Detach Role From Credential](actions/detach-role-from-credential.md) | PUT | Updates an MQTT credential in HiveMQ Cloud by detaching a role. |
| [Get MQTT Credential](actions/get-mqtt-credential.md) | GET | Retrieves an MQTT credential from HiveMQ Cloud by username. |
| [List MQTT Credentials](actions/list-mqtt-credentials.md) | GET | Retrieves MQTT credentials from HiveMQ Cloud. |

### Mqtt Permission

| Action | Method | Description |
| --- | --- | --- |
| [Create MQTT Permission](actions/create-mqtt-permission.md) | POST | Creates a new MQTT permission in HiveMQ Cloud. |
| [Delete MQTT Permission](actions/delete-mqtt-permission.md) | DELETE | Deletes an existing MQTT permission from HiveMQ Cloud. |
| [List MQTT Permissions](actions/list-mqtt-permissions.md) | GET | Retrieves MQTT permissions from HiveMQ Cloud. |
| [List Permissions By Role](actions/list-permissions-by-role.md) | GET | Retrieves permissions for an MQTT role in HiveMQ Cloud. |
| [List Role Permissions](actions/list-role-permissions.md) | GET | Retrieves MQTT role permissions from HiveMQ Cloud. |
| [Update MQTT Permission](actions/update-mqtt-permission.md) | PUT | Updates an existing MQTT permission in HiveMQ Cloud. |

### Mqtt Role

| Action | Method | Description |
| --- | --- | --- |
| [Attach Permission To Role](actions/attach-permission-to-role.md) | PUT | Updates an MQTT role in HiveMQ Cloud by attaching a permission. |
| [Create MQTT Role](actions/create-mqtt-role.md) | POST | Creates a new MQTT role in HiveMQ Cloud. |
| [Delete MQTT Role](actions/delete-mqtt-role.md) | DELETE | Deletes an existing MQTT role from HiveMQ Cloud. |
| [Detach Permission From Role](actions/detach-permission-from-role.md) | PUT | Updates an MQTT role in HiveMQ Cloud by detaching a permission. |
| [List Credential Roles](actions/list-credential-roles.md) | GET | Retrieves roles for an MQTT credential in HiveMQ Cloud. |
| [List MQTT Roles](actions/list-mqtt-roles.md) | GET | Retrieves MQTT roles from HiveMQ Cloud. |
| [Update MQTT Role](actions/update-mqtt-role.md) | PUT | Updates an existing MQTT role in HiveMQ Cloud. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Get ESE Global Role](actions/get-ese-global-role.md) | GET |  |

