# <img src="https://images.mindcloud.co/apps/icons/confluent_1781642181914.png" alt="Confluent logo" width="28" height="28"> Confluent: Universal API

Manage Confluent Cloud resources, users, API keys, and networking

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/confluent/latest
- **Category:** IT Operations / DevOps
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://confluent.cloud
- **Vendor API docs:** https://docs.confluent.io/cloud/current/api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST | Creates a new API key in Confluent Cloud. |
| [Delete API Key](actions/delete-api-key.md) | DELETE | Deletes an existing API key from Confluent Cloud. |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves API keys from Confluent Cloud. |
| [Read API Key](actions/read-api-key.md) | GET | Retrieves an API key from Confluent Cloud. |
| [Update API Key](actions/update-api-key.md) | PUT | Updates an existing API key in Confluent Cloud. |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Create Environment](actions/create-environment.md) | POST | Creates a new environment in Confluent Cloud. |
| [Delete Environment](actions/delete-environment.md) | DELETE | Deletes an existing environment from Confluent Cloud. |
| [List Environments](actions/list-environments.md) | GET | Retrieves environments from your Confluent Cloud organization. |
| [Read Environment](actions/read-environment.md) | GET | Retrieves an environment from Confluent Cloud. |
| [Update Environment](actions/update-environment.md) | PUT | Updates an existing environment in Confluent Cloud. |

### Ip Filter

| Action | Method | Description |
| --- | --- | --- |
| [Create IP Filter](actions/create-ip-filter.md) | POST | Creates a new IP filter in Confluent Cloud. |
| [Delete IP Filter](actions/delete-ip-filter.md) | DELETE | Deletes an existing IP filter from Confluent Cloud. |
| [List IP Filters](actions/list-ip-filters.md) | GET | Retrieves IP filters from Confluent Cloud. |
| [Read IP Filter](actions/read-ip-filter.md) | GET | Retrieves an IP filter from Confluent Cloud. |
| [Update IP Filter](actions/update-ip-filter.md) | PUT | Updates an existing IP filter in Confluent Cloud. |

### Ip Group

| Action | Method | Description |
| --- | --- | --- |
| [Create IP Group](actions/create-ip-group.md) | POST | Creates a new IP group in Confluent Cloud. |
| [Delete IP Group](actions/delete-ip-group.md) | DELETE | Deletes an existing IP group from Confluent Cloud. |
| [List IP Groups](actions/list-ip-groups.md) | GET | Retrieves IP groups from Confluent Cloud. |
| [Read IP Group](actions/read-ip-group.md) | GET | Retrieves an IP group from Confluent Cloud. |
| [Update IP Group](actions/update-ip-group.md) | PUT | Updates an existing IP group in Confluent Cloud. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from your Confluent Cloud account. |
| [Read Organization](actions/read-organization.md) | GET | Retrieves an organization from your Confluent Cloud account. |

### Role Binding

| Action | Method | Description |
| --- | --- | --- |
| [List Role Bindings](actions/list-role-bindings.md) | GET | Retrieves role bindings from Confluent Cloud. |
| [Read Role Binding](actions/read-role-binding.md) | GET | Retrieves a role binding from Confluent Cloud. |

### Service Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Account](actions/create-service-account.md) | POST | Creates a new service account in Confluent Cloud. |
| [Delete Service Account](actions/delete-service-account.md) | DELETE | Deletes an existing service account from Confluent Cloud. |
| [List Service Accounts](actions/list-service-accounts.md) | GET | Retrieves service accounts from Confluent Cloud. |
| [Read Service Account](actions/read-service-account.md) | GET | Retrieves a service account from Confluent Cloud. |
| [Update Service Account](actions/update-service-account.md) | PUT | Updates an existing service account in Confluent Cloud. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from your Confluent Cloud organization. |
| [Read User](actions/read-user.md) | GET | Retrieves a user from Confluent Cloud. |

