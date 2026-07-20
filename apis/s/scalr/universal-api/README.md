# <img src="https://images.mindcloud.co/apps/icons/f59535d-small-scalr-logo-only_1774986894448.png" alt="Scalr logo" width="28" height="28"> Scalr: Universal API

Manage Terraform and OpenTofu automation with policy controls, isolated environments, and governance for cloud infrastructure.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scalr/latest
- **Category:** IT Operations / DevOps
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scalr.com/
- **Vendor API docs:** https://docs.scalr.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scalr/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Access Token](actions/create-access-token.md) | POST | Creates a new access token in Scalr. |
| [Delete Access Token](actions/delete-access-token.md) | DELETE | Deletes an access token from Scalr. |
| [Get Access Token](actions/get-access-token.md) | GET | Retrieves an access token from Scalr. |
| [List Access Tokens](actions/list-access-tokens.md) | GET | Retrieves access tokens from Scalr. |
| [Update Access Token](actions/update-access-token.md) | PUT | Updates an existing access token in Scalr. |

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Scalr. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Scalr. |

### Account Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Metrics](actions/get-account-metrics.md) | GET | Retrieves account metrics from Scalr. |

### Account User

| Action | Method | Description |
| --- | --- | --- |
| [List Account Users](actions/list-account-users.md) | GET | Retrieves account users from Scalr. |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Create Environment](actions/create-environment.md) | POST | Creates a new environment in Scalr. |
| [Delete Environment](actions/delete-environment.md) | DELETE | Deletes an environment from Scalr. |
| [Get Environment](actions/get-environment.md) | GET | Retrieves an environment from Scalr. |
| [List Environments](actions/list-environments.md) | GET | Retrieves environments from Scalr. |
| [Lock Environment](actions/lock-environment.md) | PUT | Locks an environment in Scalr. |
| [Unlock Environment](actions/unlock-environment.md) | PUT | Unlocks an environment in Scalr. |
| [Update Environment](actions/update-environment.md) | PUT | Updates an existing environment in Scalr. |

### Service Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Account](actions/create-service-account.md) | POST | Creates a new service account in Scalr. |
| [Delete Service Account](actions/delete-service-account.md) | DELETE | Deletes a service account from Scalr. |
| [Get Service Account](actions/get-service-account.md) | GET | Retrieves a service account from Scalr. |
| [List Service Accounts](actions/list-service-accounts.md) | GET | Retrieves service accounts from Scalr. |

