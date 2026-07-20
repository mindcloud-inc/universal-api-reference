# <img src="https://images.mindcloud.co/apps/icons/checkmk_1777062583406.png" alt="Checkmk logo" width="28" height="28"> Checkmk: Universal API

Checkmk is an infrastructure and application monitoring platform. This app wraps the Checkmk REST API for host, service, folder, group, downtime, acknowledgement, comment, metric, audit log, activation, and discovery workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/checkmk/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://checkmk.com/
- **Vendor API docs:** https://docs.checkmk.com/latest/en/rest_api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Activation Run](actions/get-activation-run.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/get-activation-run?connectionId=$CONNECTION_ID&activationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge Host Problems](actions/acknowledge-host-problems.md) | POST | Creates host problem acknowledgements in Checkmk. |
| [Activate Changes](actions/activate-changes.md) | POST | Starts a pending changes activation run in Checkmk. |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Checkmk. |
| [Create Host](actions/create-host.md) | POST | Creates a new host in Checkmk. |
| [Create Host Downtime](actions/create-host-downtime.md) | POST | Creates a host-related scheduled downtime in Checkmk. |
| [Create Host Group](actions/create-host-group.md) | POST | Creates a new host group in Checkmk. |
| [Create Service Group](actions/create-service-group.md) | POST | Creates a new service group in Checkmk. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes an existing folder from Checkmk. |
| [Delete Host](actions/delete-host.md) | DELETE | Deletes an existing host from Checkmk. |
| [Delete Host Group](actions/delete-host-group.md) | DELETE | Deletes an existing host group from Checkmk. |
| [Get Activation Run](actions/get-activation-run.md) | GET | Retrieves activation run details from Checkmk. |
| [Get API Version](actions/get-api-version.md) | GET | Retrieves API version details from Checkmk. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves folder configuration details from Checkmk. |
| [Get Host Config](actions/get-host-config.md) | GET | Retrieves host configuration details from Checkmk. |
| [Get Host Group](actions/get-host-group.md) | GET | Retrieves host group details from Checkmk. |
| [List Audit Log](actions/list-audit-log.md) | GET | Retrieves audit log entries from Checkmk. |
| [List Downtimes](actions/list-downtimes.md) | GET | Retrieves scheduled downtime records from Checkmk. |
| [List Folder Hosts](actions/list-folder-hosts.md) | GET | Retrieves host records from a Checkmk folder. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folder configuration records from Checkmk. |
| [List Host Configs](actions/list-host-configs.md) | GET | Retrieves host configuration records from Checkmk. |
| [List Host Groups](actions/list-host-groups.md) | GET | Retrieves host group records from Checkmk. |
| [List Host Services](actions/list-host-services.md) | GET | Retrieves monitored service records for a Checkmk host. |
| [List Pending Changes](actions/list-pending-changes.md) | GET | Retrieves pending change records from Checkmk. |
| [List Service Groups](actions/list-service-groups.md) | GET | Retrieves service group records from Checkmk. |
| [List Services](actions/list-services.md) | GET | Retrieves monitored service records from Checkmk. |
| [Move Host](actions/move-host.md) | PUT | Moves an existing host to another Checkmk folder. |
| [Rename Host](actions/rename-host.md) | PUT | Renames an existing host in Checkmk. |
| [Show Host Service](actions/show-host-service.md) | GET | Retrieves monitored service details for a Checkmk host. |
| [Update Host](actions/update-host.md) | PUT | Updates an existing host in Checkmk. |
| [Update Host Group](actions/update-host-group.md) | PUT | Updates an existing host group in Checkmk. |

