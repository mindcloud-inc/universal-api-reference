# <img src="https://images.mindcloud.co/apps/icons/clip-path-group-3_1781897072793.png" alt="Grafana logo" width="28" height="28"> Grafana: Universal API

Create and inspect Grafana Cloud resources through the Grafana HTTP API using a service account token.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/grafana/latest
- **Category:** IT Operations / Observability
- **Actions:** 46
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://grafana.com
- **Vendor API docs:** https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (46)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Export Alert Rule](actions/export-alert-rule.md) | GET | Exports an alert rule from Grafana. |
| [Export Alert Rule Group](actions/export-alert-rule-group.md) | GET | Exports an alert rule group from Grafana. |
| [Export All Alert Rules](actions/export-all-alert-rules.md) | GET | Exports all alert rules from Grafana. |
| [Get Alert Rule](actions/get-alert-rule.md) | GET | Retrieves an alert rule from Grafana. |
| [Get Alert Rule Group](actions/get-alert-rule-group.md) | GET | Retrieves an alert rule group from Grafana. |
| [List Alert Rules](actions/list-alert-rules.md) | GET | Finds alert rules in Grafana. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [List Playlists](actions/list-playlists.md) | GET | Finds playlists in Grafana. |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [Get Dashboard By UID](actions/get-dashboard-by-uid.md) | GET | Retrieves a dashboard from Grafana by UID. |
| [Get Dashboard Version By UID](actions/get-dashboard-version-by-uid.md) | GET | Retrieves a dashboard version from Grafana by UID. |
| [Get Dashboard Versions By UID](actions/get-dashboard-versions-by-uid.md) | GET | Retrieves dashboard versions from Grafana by UID. |
| [List Search Sort Options](actions/list-search-sort-options.md) | GET | Retrieves search sort options from Grafana. |
| [Search Resources](actions/search-resources.md) | GET | Finds folders and dashboards in Grafana by query. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Source By Name](actions/get-data-source-by-name.md) | GET | Retrieves a data source from Grafana by name. |
| [Get Data Source By UID](actions/get-data-source-by-uid.md) | GET | Retrieves a data source from Grafana by UID. |
| [Get Data Source ID By Name](actions/get-data-source-id-by-name.md) | GET | Retrieves a data source ID from Grafana by name. |
| [List Data Sources](actions/list-data-sources.md) | GET | Finds data sources in Grafana. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Get Folder By UID](actions/get-folder-by-uid.md) | GET | Retrieves a folder from Grafana by UID. |
| [Get Folder Descendant Counts](actions/get-folder-descendant-counts.md) | GET | Retrieves descendant counts for a folder in Grafana. |
| [List Folders](actions/list-folders.md) | GET | Finds folders in Grafana. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Library Element By Name](actions/get-library-element-by-name.md) | GET | Retrieves a library element from Grafana by name. |
| [Get Library Element By UID](actions/get-library-element-by-uid.md) | GET | Retrieves a library element from Grafana by UID. |
| [Get Library Element Connections](actions/get-library-element-connections.md) | GET | Retrieves library element connections from Grafana. |
| [Get Playlist Items](actions/get-playlist-items.md) | GET | Retrieves playlist items from Grafana. |
| [List Library Elements](actions/list-library-elements.md) | GET | Finds library elements in Grafana. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Get Annotation By ID](actions/get-annotation-by-id.md) | GET | Retrieves an annotation from Grafana by ID. |
| [List Annotations](actions/list-annotations.md) | GET | Finds annotations in Grafana. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Export Contact Points](actions/export-contact-points.md) | GET | Exports contact points from Grafana. |
| [List Contact Points](actions/list-contact-points.md) | GET | Finds contact points in Grafana. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Preferences](actions/get-organization-preferences.md) | GET | Retrieves organization preferences from Grafana. |
| [List User Organizations](actions/list-user-organizations.md) | GET | Finds organizations for the current user in Grafana. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [Get Folder Permissions](actions/get-folder-permissions.md) | GET | Retrieves folder permissions from Grafana. |

### Policies

| Action | Method | Description |
| --- | --- | --- |
| [Export Notification Policy Tree](actions/export-notification-policy-tree.md) | GET | Exports the notification policy tree from Grafana. |
| [Get Notification Policy Tree](actions/get-notification-policy-tree.md) | GET | Retrieves the notification policy tree from Grafana. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Export Mute Timings](actions/export-mute-timings.md) | GET | Exports mute timings from Grafana. |
| [Get Mute Timing](actions/get-mute-timing.md) | GET | Retrieves a mute timing from Grafana. |
| [List Mute Timings](actions/list-mute-timings.md) | GET | Finds mute timings in Grafana. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Source Health](actions/get-data-source-health.md) | GET | Retrieves data source health from Grafana. |
| [Get Health](actions/get-health.md) | GET | Retrieves instance health status from Grafana. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Dashboard Tags](actions/get-dashboard-tags.md) | GET | Retrieves dashboard tags from Grafana. |
| [List Annotation Tags](actions/list-annotation-tags.md) | GET | Retrieves annotation tags from Grafana. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List User Teams](actions/list-user-teams.md) | GET | Finds teams for the current user in Grafana. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Grafana. |
| [List Templates](actions/list-templates.md) | GET | Finds templates in Grafana. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Grafana. |
| [Get User Preferences](actions/get-user-preferences.md) | GET | Retrieves user preferences from Grafana. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [Get Playlist](actions/get-playlist.md) | GET | Retrieves a playlist from Grafana. |

