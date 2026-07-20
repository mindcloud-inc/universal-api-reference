# <img src="https://images.mindcloud.co/apps/icons/hookdeck_1776181681662.png" alt="Hookdeck logo" width="28" height="28"> Hookdeck: Universal API

Manage Hookdeck event gateway resources including connections, sources, destinations, events, requests, issues, metrics, and transformations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hookdeck/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hookdeck.com
- **Vendor API docs:** https://hookdeck.com/docs/api.md

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Connections](actions/get-connections.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Create Connection](actions/create-connection.md) | POST | Creates a new connection in Hookdeck. |
| [Delete Connection](actions/delete-connection.md) | DELETE | Deletes an existing connection from Hookdeck. |
| [Get Connection](actions/get-connection.md) | GET | Retrieves a connection from Hookdeck. |
| [Get Connections](actions/get-connections.md) | GET | Retrieves connections from Hookdeck. |
| [Pause Connection](actions/pause-connection.md) | PUT | Pauses a connection in Hookdeck. |
| [Unpause Connection](actions/unpause-connection.md) | PUT | Unpauses a connection in Hookdeck. |
| [Update Connection](actions/update-connection.md) | PUT | Updates an existing connection in Hookdeck. |

### Destination

| Action | Method | Description |
| --- | --- | --- |
| [Create Destination](actions/create-destination.md) | POST | Creates a new destination in Hookdeck. |
| [Delete Destination](actions/delete-destination.md) | DELETE | Deletes an existing destination from Hookdeck. |
| [Get Destination](actions/get-destination.md) | GET | Retrieves a destination from Hookdeck. |
| [Get Destinations](actions/get-destinations.md) | GET | Retrieves destinations from Hookdeck. |
| [Update Destination](actions/update-destination.md) | PUT | Updates an existing destination in Hookdeck. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Event](actions/cancel-event.md) | PUT | Cancels a pending event in Hookdeck. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Hookdeck. |
| [Get Events](actions/get-events.md) | GET | Retrieves events from Hookdeck. |
| [Get Request Events](actions/get-request-events.md) | GET | Retrieves events for a request in Hookdeck. |
| [Retry Event](actions/retry-event.md) | PUT | Retries an event in Hookdeck. |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [Get Issue](actions/get-issue.md) | GET | Retrieves an issue from Hookdeck. |
| [Get Issues](actions/get-issues.md) | GET | Retrieves issues from Hookdeck. |

### Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Request](actions/get-request.md) | GET | Retrieves a request from Hookdeck. |
| [Get Requests](actions/get-requests.md) | GET | Retrieves requests from Hookdeck. |
| [Retry Request](actions/retry-request.md) | PUT | Retries a request in Hookdeck. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Source](actions/create-source.md) | POST | Creates a new source in Hookdeck. |
| [Delete Source](actions/delete-source.md) | DELETE | Deletes an existing source from Hookdeck. |
| [Get Source](actions/get-source.md) | GET | Retrieves a source from Hookdeck. |
| [Get Sources](actions/get-sources.md) | GET | Retrieves sources from Hookdeck. |
| [Update Source](actions/update-source.md) | PUT | Updates an existing source in Hookdeck. |

