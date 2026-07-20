# MQTT: Native API Reference

A consolidated summary of MQTT's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.hivemq.com/hivemq-cloud/rest-api.html
- **OpenAPI specification:** https://docs.hivemq.com/hivemq-cloud/rest-api/specification/public-saas-openapi.yml
- **API base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`

## Authentication

### API Token

Connect with a HiveMQ Cloud REST API token generated from the cluster console.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.hivemq.com/hivemq-cloud/console.html#api-tokens)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Attach Permission To Role](actions/attach-permission-to-role.md) | `PUT /mqtt/roles/:roleId/permissions/:permissionId/attach` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Attach Role To Credential](actions/attach-role-to-credential.md) | `PUT /user/:username/roles/:roleId/attach` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Create MQTT Credential](actions/create-mqtt-credential.md) | `POST /mqtt/credentials` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Create MQTT Permission](actions/create-mqtt-permission.md) | `POST /mqtt/permissions` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Create MQTT Role](actions/create-mqtt-role.md) | `POST /mqtt/roles` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Delete MQTT Credential](actions/delete-mqtt-credential.md) | `DELETE /mqtt/credentials/username/:username` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Delete MQTT Permission](actions/delete-mqtt-permission.md) | `DELETE /mqtt/permissions/:id` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Delete MQTT Role](actions/delete-mqtt-role.md) | `DELETE /mqtt/roles/:roleId` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Detach Permission From Role](actions/detach-permission-from-role.md) | `PUT /mqtt/roles/:roleId/permissions/:permissionId/detach` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Detach Role From Credential](actions/detach-role-from-credential.md) | `PUT /user/:username/roles/:roleId/detach` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Disconnect MQTT Client](actions/disconnect-mqtt-client.md) | `DELETE /mqtt/clients/:clientId/connection` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Get Broker Metrics](actions/get-broker-metrics.md) | `GET /metrics` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Get Client Certificate](actions/get-client-certificate.md) | `GET /clients-auth/certificate` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/public-saas-openapi.yml) |
| [Get Client JWT Config](actions/get-client-jwt-config.md) | `GET /clients-auth/jwt` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/public-saas-openapi.yml) |
| [Get ESE Global Role](actions/get-ese-global-role.md) | `GET /clients-auth/ese` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Get MQTT Client](actions/get-mqtt-client.md) | `GET /mqtt/clients/:clientId` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Get MQTT Client Connection State](actions/get-mqtt-client-connection-state.md) | `GET /mqtt/clients/:clientId/connection` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Get MQTT Credential](actions/get-mqtt-credential.md) | `GET /mqtt/credentials/username/:username` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Invalidate MQTT Client Session](actions/invalidate-mqtt-client-session.md) | `DELETE /mqtt/clients/:clientId` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [List Credential Roles](actions/list-credential-roles.md) | `GET /user/:username/roles` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [List MQTT Client Subscriptions](actions/list-mqtt-client-subscriptions.md) | `GET /mqtt/clients/:clientId/subscriptions` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [List MQTT Clients](actions/list-mqtt-clients.md) | `GET /mqtt/clients` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [List MQTT Credentials](actions/list-mqtt-credentials.md) | `GET /mqtt/credentials` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [List MQTT Permissions](actions/list-mqtt-permissions.md) | `GET /mqtt/permissions` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [List MQTT Roles](actions/list-mqtt-roles.md) | `GET /mqtt/roles` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [List Permissions By Role](actions/list-permissions-by-role.md) | `GET /mqtt/roles/:roleIdOrName/permissions` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [List Role Permissions](actions/list-role-permissions.md) | `GET /mqtt/roles/permissions` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Search MQTT Clients](actions/search-mqtt-clients.md) | `GET /a/mqtt/clients/search` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Update MQTT Permission](actions/update-mqtt-permission.md) | `PUT /mqtt/permissions/:id` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
| [Update MQTT Role](actions/update-mqtt-role.md) | `PUT /mqtt/roles/:roleId` | [docs](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/) |
