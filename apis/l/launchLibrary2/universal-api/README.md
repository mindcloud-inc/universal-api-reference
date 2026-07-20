# <img src="https://images.mindcloud.co/apps/icons/ll2-logo_1777486633281.png" alt="Launch Library 2 logo" width="28" height="28"> Launch Library 2: Universal API

Public REST API from The Space Devs for rocket launches, space events, agencies, astronauts, spacecraft, pads, programs, and related spaceflight data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/launchLibrary2/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://thespacedevs.com/llapi
- **Vendor API docs:** https://ll.thespacedevs.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Agency](actions/get-agency.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-agency?connectionId=$CONNECTION_ID&id=121" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Agency

| Action | Method | Description |
| --- | --- | --- |
| [Get Agency](actions/get-agency.md) | GET |  |
| [List Agencies](actions/list-agencies.md) | GET |  |

### Astronaut

| Action | Method | Description |
| --- | --- | --- |
| [Get Astronaut](actions/get-astronaut.md) | GET |  |
| [List Astronauts](actions/list-astronauts.md) | GET |  |

### Docking Event

| Action | Method | Description |
| --- | --- | --- |
| [List Docking Events](actions/list-docking-events.md) | GET |  |

### Expedition

| Action | Method | Description |
| --- | --- | --- |
| [List Expeditions](actions/list-expeditions.md) | GET |  |

### Launch

| Action | Method | Description |
| --- | --- | --- |
| [Get Launch](actions/get-launch.md) | GET |  |
| [List Launches](actions/list-launches.md) | GET |  |
| [List Previous Launches](actions/list-previous-launches.md) | GET |  |
| [List Upcoming Launches](actions/list-upcoming-launches.md) | GET |  |

### Launch Location

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET |  |

### Launch Pad

| Action | Method | Description |
| --- | --- | --- |
| [List Pads](actions/list-pads.md) | GET |  |

### Launcher Configuration

| Action | Method | Description |
| --- | --- | --- |
| [List Launcher Configurations](actions/list-launcher-configurations.md) | GET |  |

### Payload

| Action | Method | Description |
| --- | --- | --- |
| [List Payloads](actions/list-payloads.md) | GET |  |

### Space Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET |  |
| [List Events](actions/list-events.md) | GET |  |
| [List Previous Events](actions/list-previous-events.md) | GET |  |
| [List Upcoming Events](actions/list-upcoming-events.md) | GET |  |

### Space Program

| Action | Method | Description |
| --- | --- | --- |
| [List Programs](actions/list-programs.md) | GET |  |

### Space Station

| Action | Method | Description |
| --- | --- | --- |
| [Get Space Station](actions/get-space-station.md) | GET |  |
| [List Space Stations](actions/list-space-stations.md) | GET |  |

### Spacecraft

| Action | Method | Description |
| --- | --- | --- |
| [List Spacecraft](actions/list-spacecraft.md) | GET |  |

### Spacewalk

| Action | Method | Description |
| --- | --- | --- |
| [List Spacewalks](actions/list-spacewalks.md) | GET |  |

### Update

| Action | Method | Description |
| --- | --- | --- |
| [List Updates](actions/list-updates.md) | GET |  |

