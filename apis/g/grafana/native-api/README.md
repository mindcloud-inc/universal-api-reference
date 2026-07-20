# Grafana: Native API Reference

A consolidated summary of Grafana's API configuration and 46 documented operations, with links to official documentation.

- **Official docs:** https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/
- **OpenAPI specification:** https://apps78aa.grafana.net/public/openapi3.json
- **API base URL:** `https://apps78aa.grafana.net/api`

## Authentication

### Service Account Token

Authenticate with a Grafana service account token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://grafana.com/docs/grafana/latest/developers/http_api/auth/)

## Endpoints (46 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Export Alert Rule](actions/export-alert-rule.md) | `GET /v1/provisioning/alert-rules/:UID/export` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [Export Alert Rule Group](actions/export-alert-rule-group.md) | `GET /v1/provisioning/folder/:FolderUID/rule-groups/:Group/export` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [Export All Alert Rules](actions/export-all-alert-rules.md) | `GET /v1/provisioning/alert-rules/export` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [Export Contact Points](actions/export-contact-points.md) | `GET /v1/provisioning/contact-points/export` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [Export Mute Timings](actions/export-mute-timings.md) | `GET /v1/provisioning/mute-timings/export` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [Export Notification Policy Tree](actions/export-notification-policy-tree.md) | `GET /v1/provisioning/policies/export` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [Get Alert Rule](actions/get-alert-rule.md) | `GET /v1/provisioning/alert-rules/:UID` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [Get Alert Rule Group](actions/get-alert-rule-group.md) | `GET /v1/provisioning/folder/:FolderUID/rule-groups/:Group` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [Get Annotation By ID](actions/get-annotation-by-id.md) | `GET /annotations/:annotation_id` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/annotations/) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/user/) |
| [Get Dashboard By UID](actions/get-dashboard-by-uid.md) | `GET /dashboards/uid/:uid` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/dashboard/) |
| [Get Dashboard Tags](actions/get-dashboard-tags.md) | `GET /dashboards/tags` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/dashboard/) |
| [Get Dashboard Version By UID](actions/get-dashboard-version-by-uid.md) | `GET /dashboards/uid/:uid/versions/:DashboardVersionID` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/dashboard_versions/) |
| [Get Dashboard Versions By UID](actions/get-dashboard-versions-by-uid.md) | `GET /dashboards/uid/:uid/versions` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/dashboard_versions/) |
| [Get Data Source By Name](actions/get-data-source-by-name.md) | `GET /datasources/name/:name` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/data_source/) |
| [Get Data Source By UID](actions/get-data-source-by-uid.md) | `GET /datasources/uid/:uid` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/data_source/) |
| [Get Data Source Health](actions/get-data-source-health.md) | `GET /datasources/uid/:uid/health` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/data_source/) |
| [Get Data Source ID By Name](actions/get-data-source-id-by-name.md) | `GET /datasources/id/:name` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/data_source/) |
| [Get Folder By UID](actions/get-folder-by-uid.md) | `GET /folders/:folder_uid` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/folder/) |
| [Get Folder Descendant Counts](actions/get-folder-descendant-counts.md) | `GET /folders/:folder_uid/counts` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/folder/) |
| [Get Folder Permissions](actions/get-folder-permissions.md) | `GET /folders/:folder_uid/permissions` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/folder_permissions/) |
| [Get Health](actions/get-health.md) | `GET /health` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/other/) |
| [Get Library Element By Name](actions/get-library-element-by-name.md) | `GET /library-elements/name/:library_element_name` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/library_element/) |
| [Get Library Element By UID](actions/get-library-element-by-uid.md) | `GET /library-elements/:library_element_uid` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/library_element/) |
| [Get Library Element Connections](actions/get-library-element-connections.md) | `GET /library-elements/:library_element_uid/connections/` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/library_element/) |
| [Get Mute Timing](actions/get-mute-timing.md) | `GET /v1/provisioning/mute-timings/:name` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [Get Notification Policy Tree](actions/get-notification-policy-tree.md) | `GET /v1/provisioning/policies` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [Get Organization Preferences](actions/get-organization-preferences.md) | `GET /org/preferences` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/preferences/) |
| [Get Playlist](actions/get-playlist.md) | `GET /playlists/:uid` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/playlist/) |
| [Get Playlist Items](actions/get-playlist-items.md) | `GET /playlists/:uid/items` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/playlist/) |
| [Get Template](actions/get-template.md) | `GET /v1/provisioning/templates/:name` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [Get User Preferences](actions/get-user-preferences.md) | `GET /user/preferences` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/preferences/) |
| [List Alert Rules](actions/list-alert-rules.md) | `GET /v1/provisioning/alert-rules` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [List Annotation Tags](actions/list-annotation-tags.md) | `GET /annotations/tags` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/annotations/) |
| [List Annotations](actions/list-annotations.md) | `GET /annotations` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/annotations/) |
| [List Contact Points](actions/list-contact-points.md) | `GET /v1/provisioning/contact-points` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [List Data Sources](actions/list-data-sources.md) | `GET /datasources` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/data_source/) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/folder/) |
| [List Library Elements](actions/list-library-elements.md) | `GET /library-elements` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/library_element/) |
| [List Mute Timings](actions/list-mute-timings.md) | `GET /v1/provisioning/mute-timings` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [List Playlists](actions/list-playlists.md) | `GET /playlists` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/playlist/) |
| [List Search Sort Options](actions/list-search-sort-options.md) | `GET /search/sorting` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/folder_dashboard_search/) |
| [List Templates](actions/list-templates.md) | `GET /v1/provisioning/templates` | [docs](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/) |
| [List User Organizations](actions/list-user-organizations.md) | `GET /user/orgs` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/user/) |
| [List User Teams](actions/list-user-teams.md) | `GET /user/teams` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/user/) |
| [Search Resources](actions/search-resources.md) | `GET /search` | [docs](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/folder_dashboard_search/) |
