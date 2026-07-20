# <img src="https://images.mindcloud.co/apps/icons/apideck_1776184625570.png" alt="Apideck logo" width="28" height="28"> Apideck: Universal API

Manage Apideck Vault consumers, connections, custom mappings, sessions, and logs through the official Vault API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/apideck/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.apideck.com
- **Vendor API docs:** https://developers.apideck.com/apis/vault/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get all consumers](actions/consumersall.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersall?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get all consumer request logs](actions/logsall.md) | GET | Retrieves consumer request logs from Apideck Vault. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Get consent records](actions/connectionconsentsall.md) | GET | Retrieves consent records from Apideck Vault. |
| [Update consent state](actions/connectionconsentupdate.md) | PUT | Updates a connection consent state in Apideck Vault. |
| [List connection custom mappings](actions/connectioncustommappingsall.md) | GET | Retrieves connection custom mappings from Apideck Vault. |
| [Create connection](actions/connectionsadd.md) | POST | Creates an authorized connection in Apideck Vault. |
| [Get all connections](actions/connectionsall.md) | GET | Retrieves all connections from Apideck Vault. |
| [Authorize](actions/connectionsauthorize.md) | GET | Starts an OAuth authorization flow in Apideck Vault. |
| [Callback](actions/connectionscallback.md) | GET | Handles an OAuth callback in Apideck Vault. |
| [Delete connection](actions/connectionsdelete.md) | DELETE | Deletes an existing connection from Apideck Vault. |
| [Get resource settings](actions/connectionsettingsall.md) | GET | Retrieves connection resource settings from Apideck Vault. |
| [Update settings](actions/connectionsettingsupdate.md) | PUT | Updates connection resource settings in Apideck Vault. |
| [Get resource example](actions/connectionsexample.md) | GET | Retrieves a resource example from Apideck Vault. |
| [Import connection](actions/connectionsimport.md) | POST | Imports an authorized connection into Apideck Vault. |
| [Get connection](actions/connectionsone.md) | GET | Retrieves a connection from Apideck Vault. |
| [Revoke connection](actions/connectionsrevoke.md) | GET | Starts a connection revoke flow in Apideck Vault. |
| [Get resource schema](actions/connectionsschema.md) | GET | Retrieves a resource schema from Apideck Vault. |
| [Authorize Access Token](actions/connectionstoken.md) | POST | Authorizes stored connection credentials in Apideck Vault. |
| [Update connection](actions/connectionsupdate.md) | PUT | Updates an existing connection in Apideck Vault. |
| [Create Callback State](actions/createcallbackstate.md) | POST | Creates a callback state in Apideck Vault. |
| [Get resource custom fields](actions/customfieldsall.md) | GET | Retrieves resource custom fields from Apideck Vault. |
| [Validate Connection State](actions/validateconnectionstate.md) | POST | Validates a connection state in Apideck Vault. |

### Mappings

| Action | Method | Description |
| --- | --- | --- |
| [Create custom mapping](actions/custommappingsadd.md) | POST | Creates a new custom mapping in Apideck Vault. |
| [List custom mappings](actions/custommappingsall.md) | GET | Retrieves custom mappings from Apideck Vault. |
| [Delete custom mapping](actions/custommappingsdelete.md) | DELETE | Deletes an existing custom mapping from Apideck Vault. |
| [Get custom mapping](actions/custommappingsone.md) | GET | Retrieves a custom mapping from Apideck Vault. |
| [Update custom mapping](actions/custommappingsupdate.md) | PUT | Updates an existing custom mapping in Apideck Vault. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create session](actions/sessionscreate.md) | POST | Creates a Hosted Vault session in Apideck. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Consumer request counts](actions/consumerrequestcountsall.md) | GET | Retrieves consumer request counts from Apideck Vault. |
| [Create consumer](actions/consumersadd.md) | POST | Creates a new consumer in Apideck Vault. |
| [Get all consumers](actions/consumersall.md) | GET | Retrieves all consumers from Apideck Vault. |
| [Delete consumer](actions/consumersdelete.md) | DELETE | Deletes a consumer and all their connections from Apideck Vault. |
| [Get consumer](actions/consumersone.md) | GET | Retrieves a consumer from Apideck Vault. |
| [Update consumer](actions/consumersupdate.md) | PUT | Updates an existing consumer in Apideck Vault. |

