# <img src="https://images.mindcloud.co/apps/icons/daytona-icon_1776269865430.png" alt="Daytona logo" width="28" height="28"> Daytona: Universal API

Daytona provides secure, on-demand cloud development sandboxes for running code, managing environments, and operating developer infrastructure.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/daytona/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.daytona.io
- **Vendor API docs:** https://www.daytona.io/docs/tools/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current API Key](actions/get-current-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-current-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Get Current API Key](actions/get-current-api-key.md) | GET | Retrieves the current API key details from Daytona. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Available Regions](actions/list-available-regions.md) | GET | Retrieves the available regions from Daytona. |
| [List Shared Regions](actions/list-shared-regions.md) | GET | Retrieves the shared regions from Daytona. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Sandbox Backup](actions/create-sandbox-backup.md) | POST | Creates a sandbox backup in Daytona. |
| [Create Sandbox Snapshot](actions/create-sandbox-snapshot.md) | POST | Creates a snapshot from a sandbox in Daytona. |
| [Create Sandbox SSH Access](actions/create-sandbox-ssh-access.md) | POST | Creates sandbox SSH access in Daytona. |
| [Create Snapshot](actions/create-snapshot.md) | POST | Creates a new snapshot in Daytona. |
| [Create Volume](actions/create-volume.md) | POST | Creates a new volume in Daytona. |
| [Delete Volume](actions/delete-volume.md) | DELETE | Deletes an existing volume from Daytona. |
| [Get Port Preview URL](actions/get-port-preview-url.md) | GET | Retrieves a sandbox port preview URL from Daytona. |
| [Get Sandbox Build Logs URL](actions/get-sandbox-build-logs-url.md) | GET | Retrieves the sandbox build logs URL from Daytona. |
| [Get Sandbox Metrics](actions/get-sandbox-metrics.md) | GET | Retrieves sandbox metrics from Daytona. |
| [Get Sandbox Region Quota](actions/get-sandbox-region-quota.md) | GET | Retrieves the sandbox region quota from Daytona. |
| [Get Sandbox Toolbox Proxy URL](actions/get-sandbox-toolbox-proxy-url.md) | GET | Retrieves the sandbox toolbox proxy URL from Daytona. |
| [Get Signed Port Preview URL](actions/get-signed-port-preview-url.md) | GET | Retrieves a signed sandbox port preview URL from Daytona. |
| [Get Snapshot](actions/get-snapshot.md) | GET | Retrieves snapshot details from Daytona. |
| [Get Snapshot Build Logs URL](actions/get-snapshot-build-logs-url.md) | GET | Retrieves the snapshot build logs URL from Daytona. |
| [Get Volume](actions/get-volume.md) | GET | Retrieves volume details from Daytona. |
| [List Snapshots](actions/list-snapshots.md) | GET | Retrieves all snapshots from Daytona. |
| [List Volumes](actions/list-volumes.md) | GET | Retrieves all volumes from Daytona. |
| [Revoke Sandbox SSH Access](actions/revoke-sandbox-ssh-access.md) | DELETE | Revokes sandbox SSH access in Daytona. |
| [Validate Sandbox SSH Access](actions/validate-sandbox-ssh-access.md) | GET | Validates sandbox SSH access in Daytona. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Archive Sandbox](actions/archive-sandbox.md) | PUT | Archives a sandbox in Daytona. |
| [Create Sandbox](actions/create-sandbox.md) | POST | Creates a new sandbox in Daytona. |
| [Delete Sandbox](actions/delete-sandbox.md) | DELETE | Deletes an existing sandbox from Daytona. |
| [Get Sandbox](actions/get-sandbox.md) | GET | Retrieves sandbox details from Daytona. |
| [List Sandboxes Paginated](actions/list-sandboxes-paginated.md) | GET | Retrieves a paginated list of sandboxes from Daytona. |
| [Recover Sandbox](actions/recover-sandbox.md) | PUT | Recovers a sandbox from an error state in Daytona. |
| [Replace Sandbox Labels](actions/replace-sandbox-labels.md) | PUT | Replaces sandbox labels in Daytona. |
| [Set Sandbox Autostop Interval](actions/set-sandbox-autostop-interval.md) | PUT | Updates the sandbox autostop interval in Daytona. |
| [Start Sandbox](actions/start-sandbox.md) | PUT | Starts or resumes a sandbox in Daytona. |
| [Stop Sandbox](actions/stop-sandbox.md) | PUT | Stops a sandbox in Daytona. |
| [Update Sandbox Public Status](actions/update-sandbox-public-status.md) | PUT | Updates the sandbox public status in Daytona. |

