# Merge Agent Handler: Native API Reference

A consolidated summary of Merge Agent Handler's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.merge.dev/merge-agent-handler/agent-handler
- **API base URL:** `https://ah-api.merge.dev/api/v1`

## Authentication

### API Key

Authenticate requests with a Merge Agent Handler production or test access key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.merge.dev/merge-agent-handler/admin-setup/authentication)

## Pagination

Use `page_size` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Upsert Connector Tool Description Overrides](actions/bulk-upsert-connector-tool-description-overrides.md) | `PATCH /connectors/tool-description-overrides/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/tool-description-overrides/bulk-upsert-delete) |
| [Bulk Upsert Tool Pack Tool Description Overrides](actions/bulk-upsert-tool-pack-tool-description-overrides.md) | `PATCH /tool-packs/:tool_pack_id/tool-description-overrides/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/tool-description-overrides/bulk-upsert-delete-tool-pack) |
| [Create Application Credential](actions/create-application-credential.md) | `POST /application-credentials/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/application-credentials/create) |
| [Create Custom Regex Rule](actions/create-custom-regex-rule.md) | `POST /security/custom-regex-rules/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/custom-regex-rules/create-custom-regex-rule) |
| [Create Registered User](actions/create-registered-user.md) | `POST /registered-users/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/registered-users/create) |
| [Create Registered User Link Token](actions/create-registered-user-link-token.md) | `POST /registered-users/:registered_user_id/link-token/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/link-token/create-for-registered-user) |
| [Create Tool Pack](actions/create-tool-pack.md) | `POST /tool-packs/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/tool-packs/create) |
| [Create Tool Pack Custom Regex Rule](actions/create-tool-pack-custom-regex-rule.md) | `POST /tool-packs/:tool_pack_id/custom-regex-rules/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/custom-regex-rules/create-custom-regex-rule-tool-pack) |
| [Delete Application Credential](actions/delete-application-credential.md) | `DELETE /application-credentials/:id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/application-credentials/destroy) |
| [Delete Custom Regex Rule](actions/delete-custom-regex-rule.md) | `DELETE /security/custom-regex-rules/:rule_id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/custom-regex-rules/delete-custom-regex-rule) |
| [Delete Registered User](actions/delete-registered-user.md) | `DELETE /registered-users/:registered_user_id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/registered-users/destroy) |
| [Delete Tool Pack](actions/delete-tool-pack.md) | `DELETE /tool-packs/:tool_pack_id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/tool-packs/destroy) |
| [Delete Tool Pack Custom Regex Rule](actions/delete-tool-pack-custom-regex-rule.md) | `DELETE /tool-packs/:tool_pack_id/custom-regex-rules/:rule_id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/custom-regex-rules/delete-custom-regex-rule-tool-pack) |
| [Delete Tool Pack Standard Entity Rule Override](actions/delete-tool-pack-standard-entity-rule-override.md) | `DELETE /tool-packs/:tool_pack_id/standard-entity-rules/:entity_type/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/standard-entity-rules/delete-standard-entity-rule-override-tool-pack) |
| [Disconnect Registered User Connector](actions/disconnect-registered-user-connector.md) | `DELETE /credentials/registered-users/:registered_user_id/connectors/:connector_slug/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/credentials/registered-users-connectors-destroy) |
| [Execute MCP Request](actions/execute-mcp-request.md) | `POST /tool-packs/:tool_pack_id/registered-users/:registered_user_id/mcp/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/mcp/endpoint-post) |
| [Get Application Credential](actions/get-application-credential.md) | `GET /application-credentials/:id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/application-credentials/retrieve) |
| [Get Connector](actions/get-connector.md) | `GET /connectors/:connector_slug/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/connectors/retrieve) |
| [Get Custom Regex Rule](actions/get-custom-regex-rule.md) | `GET /security/custom-regex-rules/:rule_id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/custom-regex-rules/get-custom-regex-rule) |
| [Get Registered User](actions/get-registered-user.md) | `GET /registered-users/:registered_user_id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/registered-users/retrieve) |
| [Get Tool Pack](actions/get-tool-pack.md) | `GET /tool-packs/:tool_pack_id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/tool-packs/retrieve) |
| [List Application Credentials](actions/list-application-credentials.md) | `GET /application-credentials/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/application-credentials/list) |
| [List Audit Logs](actions/list-audit-logs.md) | `GET /audit-log/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/audit-log/list) |
| [List Connector Tool Description Overrides](actions/list-connector-tool-description-overrides.md) | `GET /connectors/tool-description-overrides/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/tool-description-overrides/list) |
| [List Connectors](actions/list-connectors.md) | `GET /connectors/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/connectors/list) |
| [List Custom Regex Rules](actions/list-custom-regex-rules.md) | `GET /security/custom-regex-rules/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/custom-regex-rules/list-custom-regex-rules) |
| [List Registered Users](actions/list-registered-users.md) | `GET /registered-users/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/registered-users/list) |
| [List Standard Entity Rules](actions/list-standard-entity-rules.md) | `GET /security/standard-entity-rules/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/standard-entity-rules/list-standard-entity-rules) |
| [List Tool Pack Custom Regex Rules](actions/list-tool-pack-custom-regex-rules.md) | `GET /tool-packs/:tool_pack_id/custom-regex-rules/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/custom-regex-rules/list-custom-regex-rules-tool-pack) |
| [List Tool Pack Standard Entity Rules](actions/list-tool-pack-standard-entity-rules.md) | `GET /tool-packs/:tool_pack_id/standard-entity-rules/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/standard-entity-rules/list-standard-entity-rules-tool-pack) |
| [List Tool Pack Tool Description Overrides](actions/list-tool-pack-tool-description-overrides.md) | `GET /tool-packs/:tool_pack_id/tool-description-overrides/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/tool-description-overrides/list-tool-pack) |
| [List Tool Packs](actions/list-tool-packs.md) | `GET /tool-packs/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/tool-packs/list) |
| [Search Tools](actions/search-tools.md) | `POST /tool-packs/:tool_pack_id/registered-users/:registered_user_id/search/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/tool-search/search-tools) |
| [Update Application Credential](actions/update-application-credential.md) | `PATCH /application-credentials/:id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/application-credentials/partial-update) |
| [Update Custom Regex Rule](actions/update-custom-regex-rule.md) | `PATCH /security/custom-regex-rules/:rule_id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/custom-regex-rules/update-custom-regex-rule) |
| [Update Registered User](actions/update-registered-user.md) | `PATCH /registered-users/:registered_user_id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/registered-users/partial-update) |
| [Update Standard Entity Rule](actions/update-standard-entity-rule.md) | `PUT /security/standard-entity-rules/:entity_type/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/standard-entity-rules/update-standard-entity-rule) |
| [Update Tool Pack](actions/update-tool-pack.md) | `PATCH /tool-packs/:tool_pack_id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/tool-packs/partial-update) |
| [Update Tool Pack Custom Regex Rule](actions/update-tool-pack-custom-regex-rule.md) | `PATCH /tool-packs/:tool_pack_id/custom-regex-rules/:rule_id/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/custom-regex-rules/update-custom-regex-rule-tool-pack) |
| [Upsert Tool Pack Standard Entity Rule Override](actions/upsert-tool-pack-standard-entity-rule-override.md) | `PUT /tool-packs/:tool_pack_id/standard-entity-rules/:entity_type/` | [docs](https://docs.merge.dev/merge-agent-handler/agent-handler/standard-entity-rules/upsert-standard-entity-rule-override-tool-pack) |
