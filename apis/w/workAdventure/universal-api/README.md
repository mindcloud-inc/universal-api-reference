# <img src="https://images.mindcloud.co/apps/icons/workadventure-icon_1776954646234.png" alt="WorkAdventure logo" width="28" height="28"> WorkAdventure: Universal API

WorkAdventure is a collaborative virtual world platform. This app wraps the WorkAdventure inbound API and supported map-storage HTTP endpoints for world, member, and map-management workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/workAdventure/latest
- **Category:** Communication / Video Communications
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://workadventu.re
- **Vendor API docs:** https://docs.workadventu.re/developer/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping map storage](actions/ping-map-storage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/ping-map-storage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Archive

| Action | Method | Description |
| --- | --- | --- |
| [Download map archive](actions/download-map-archive.md) | GET | Downloads a directory archive from WorkAdventure map storage. |

### Map

| Action | Method | Description |
| --- | --- | --- |
| [List maps](actions/list-maps.md) | GET | Retrieves the cached map inventory for a WorkAdventure world. |
| [Validate map](actions/validate-map.md) | GET | Validates a map URL in WorkAdventure. |

### Map Archive

| Action | Method | Description |
| --- | --- | --- |
| [Upload map archive](actions/upload-map-archive.md) | POST | Uploads a ZIP archive to WorkAdventure map storage. |

### Map File

| Action | Method | Description |
| --- | --- | --- |
| [Copy map file](actions/copy-map-file.md) | POST | Copies a file in WorkAdventure map storage. |
| [Delete map file](actions/delete-map-file.md) | DELETE | Deletes a file from WorkAdventure map storage. |
| [Move map file](actions/move-map-file.md) | PUT | Moves a file in WorkAdventure map storage. |

### Map Storage

| Action | Method | Description |
| --- | --- | --- |
| [Ping map storage](actions/ping-map-storage.md) | GET | Checks whether WorkAdventure map storage is reachable. |

### Map Storage Index

| Action | Method | Description |
| --- | --- | --- |
| [Get map storage index](actions/get-map-storage-index.md) | GET | Retrieves the WorkAdventure map storage index endpoint. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Create member](actions/create-member.md) | POST | Creates a member in a WorkAdventure world. |
| [Delete member](actions/delete-member.md) | DELETE | Deletes a member from a WorkAdventure world. |
| [Get member](actions/get-member.md) | GET | Retrieves a member from a WorkAdventure world. |
| [List members](actions/list-members.md) | GET | Retrieves members from a WorkAdventure world. |
| [Update member](actions/update-member.md) | PUT | Updates a member in a WorkAdventure world. |

### Private File

| Action | Method | Description |
| --- | --- | --- |
| [Get private file](actions/get-private-file.md) | GET | Retrieves a private file from WorkAdventure map storage. |

### Stored File

| Action | Method | Description |
| --- | --- | --- |
| [Get file](actions/get-file.md) | GET | Retrieves a file from WorkAdventure map storage. |
| [Upload file](actions/upload-file.md) | PUT | Uploads or replaces a file in WorkAdventure map storage. |

### Wam File

| Action | Method | Description |
| --- | --- | --- |
| [Get WAM file](actions/get-wam-file.md) | GET | Retrieves a WAM file from WorkAdventure map storage. |
| [Upload WAM file](actions/upload-wam-file.md) | PUT | Uploads or replaces a WAM file in WorkAdventure map storage. |

### World

| Action | Method | Description |
| --- | --- | --- |
| [Get world details](actions/get-world-details.md) | GET | Retrieves details for a WorkAdventure world by slug. |

