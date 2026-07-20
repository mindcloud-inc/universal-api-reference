# <img src="https://images.mindcloud.co/apps/icons/merge-agent-handler_1775846919597.png" alt="Merge Agent Handler logo" width="28" height="28"> Merge Agent Handler: Universal API

Merge Agent Handler lets AI agents access third-party tools through registered users, connectors, tool packs, tool search, and MCP execution.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mergeAgentHandler/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.merge.dev
- **Vendor API docs:** https://docs.merge.dev/merge-agent-handler/agent-handler

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tool Packs](actions/list-tool-packs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/list-tool-packs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create Registered User Link Token](actions/create-registered-user-link-token.md) | POST | Creates a registered user link token in Merge Agent Handler. |

### Application Credential

| Action | Method | Description |
| --- | --- | --- |
| [Create Application Credential](actions/create-application-credential.md) | POST | Creates an application credential in Merge Agent Handler. |
| [Delete Application Credential](actions/delete-application-credential.md) | DELETE | Deletes an application credential from Merge Agent Handler. |
| [Get Application Credential](actions/get-application-credential.md) | GET | Retrieves an application credential from Merge Agent Handler. |
| [List Application Credentials](actions/list-application-credentials.md) | GET | Retrieves application credentials from Merge Agent Handler. |
| [Update Application Credential](actions/update-application-credential.md) | PUT | Updates an application credential in Merge Agent Handler. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [List Audit Logs](actions/list-audit-logs.md) | GET | Retrieves audit log events from Merge Agent Handler. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Disconnect Registered User Connector](actions/disconnect-registered-user-connector.md) | DELETE | Disconnects a registered user's connector in Merge Agent Handler. |

### Connectors

| Action | Method | Description |
| --- | --- | --- |
| [Get Connector](actions/get-connector.md) | GET | Retrieves a connector from Merge Agent Handler. |
| [List Connectors](actions/list-connectors.md) | GET | Retrieves connectors from Merge Agent Handler. |

### Custom Regex Rule

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Regex Rule](actions/create-custom-regex-rule.md) | POST | Creates a custom regex rule in Merge Agent Handler. |
| [Create Tool Pack Custom Regex Rule](actions/create-tool-pack-custom-regex-rule.md) | POST | Creates a tool pack custom regex rule in Merge Agent Handler. |
| [Delete Custom Regex Rule](actions/delete-custom-regex-rule.md) | DELETE | Deletes a custom regex rule from Merge Agent Handler. |
| [Delete Tool Pack Custom Regex Rule](actions/delete-tool-pack-custom-regex-rule.md) | DELETE | Deletes a tool pack custom regex rule from Merge Agent Handler. |
| [Get Custom Regex Rule](actions/get-custom-regex-rule.md) | GET | Retrieves a custom regex rule from Merge Agent Handler. |
| [List Custom Regex Rules](actions/list-custom-regex-rules.md) | GET | Retrieves custom regex rules from Merge Agent Handler. |
| [List Tool Pack Custom Regex Rules](actions/list-tool-pack-custom-regex-rules.md) | GET | Retrieves tool pack custom regex rules from Merge Agent Handler. |
| [Update Custom Regex Rule](actions/update-custom-regex-rule.md) | PUT | Updates a custom regex rule in Merge Agent Handler. |
| [Update Tool Pack Custom Regex Rule](actions/update-tool-pack-custom-regex-rule.md) | PUT | Updates a tool pack custom regex rule in Merge Agent Handler. |

### Mcp Request

| Action | Method | Description |
| --- | --- | --- |
| [Execute MCP Request](actions/execute-mcp-request.md) | POST | Executes an MCP request in Merge Agent Handler. |

### Standard Entity Rule

| Action | Method | Description |
| --- | --- | --- |
| [Delete Tool Pack Standard Entity Rule Override](actions/delete-tool-pack-standard-entity-rule-override.md) | DELETE | Deletes a tool pack standard entity rule override from Merge Agent Handler. |
| [List Standard Entity Rules](actions/list-standard-entity-rules.md) | GET | Retrieves standard entity rules from Merge Agent Handler. |
| [List Tool Pack Standard Entity Rules](actions/list-tool-pack-standard-entity-rules.md) | GET | Retrieves tool pack standard entity rules from Merge Agent Handler. |
| [Update Standard Entity Rule](actions/update-standard-entity-rule.md) | PUT | Updates a standard entity rule in Merge Agent Handler. |
| [Upsert Tool Pack Standard Entity Rule Override](actions/upsert-tool-pack-standard-entity-rule-override.md) | PUT | Creates or updates a tool pack standard entity rule override in Merge Agent Handler. |

### Tool Description Override

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Upsert Connector Tool Description Overrides](actions/bulk-upsert-connector-tool-description-overrides.md) | PUT | Upserts or deletes connector tool description overrides in Merge Agent Handler. |
| [Bulk Upsert Tool Pack Tool Description Overrides](actions/bulk-upsert-tool-pack-tool-description-overrides.md) | PUT | Upserts or deletes tool pack description overrides in Merge Agent Handler. |
| [List Connector Tool Description Overrides](actions/list-connector-tool-description-overrides.md) | GET | Retrieves connector tool description overrides from Merge Agent Handler. |
| [List Tool Pack Tool Description Overrides](actions/list-tool-pack-tool-description-overrides.md) | GET | Retrieves tool pack description overrides from Merge Agent Handler. |

### Tool Pack

| Action | Method | Description |
| --- | --- | --- |
| [Create Tool Pack](actions/create-tool-pack.md) | POST | Creates a tool pack in Merge Agent Handler. |
| [Delete Tool Pack](actions/delete-tool-pack.md) | DELETE | Deletes a tool pack from Merge Agent Handler. |
| [Get Tool Pack](actions/get-tool-pack.md) | GET | Retrieves a tool pack from Merge Agent Handler. |
| [List Tool Packs](actions/list-tool-packs.md) | GET | Retrieves tool packs from Merge Agent Handler. |
| [Update Tool Pack](actions/update-tool-pack.md) | PUT | Updates a tool pack in Merge Agent Handler. |

### Tool Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Tools](actions/search-tools.md) | POST | Finds tools in Merge Agent Handler by user intent. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Registered User](actions/create-registered-user.md) | POST | Creates a registered user in Merge Agent Handler. |
| [Delete Registered User](actions/delete-registered-user.md) | DELETE | Deletes a registered user from Merge Agent Handler. |
| [Get Registered User](actions/get-registered-user.md) | GET | Retrieves a registered user from Merge Agent Handler. |
| [List Registered Users](actions/list-registered-users.md) | GET | Retrieves registered users from Merge Agent Handler. |
| [Update Registered User](actions/update-registered-user.md) | PUT | Updates a registered user in Merge Agent Handler. |

