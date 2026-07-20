# Launch Library 2: Native API Reference

A consolidated summary of Launch Library 2's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://ll.thespacedevs.com/docs/
- **API base URL:** `https://ll.thespacedevs.com/2.3.0/`

## Authentication

### No Authentication

The documented public Launch Library 2 REST API path does not require provider-managed credentials for the normal free-tier read endpoints.

This API does not require request authentication.

[Official authentication documentation](https://thespacedevs.com/llapi)

## API conventions

Responses from this API use JSON. Response data is read from `results`. The next-page cursor is read from `next`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `gt`, `gte`, `lt`, `lte`.

## Sorting

Set the sort field with `ordering` in the query string. Use `ascending` for ascending order and `-` for descending order. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Agency](actions/get-agency.md) | `GET agencies/{{id}}/` | [docs](https://ll.thespacedevs.com/2.3.0/agencies/?format=api) |
| [Get Astronaut](actions/get-astronaut.md) | `GET astronauts/{{id}}/` | [docs](https://ll.thespacedevs.com/2.3.0/astronauts/?format=api) |
| [Get Event](actions/get-event.md) | `GET events/{{id}}/` | [docs](https://ll.thespacedevs.com/2.3.0/events/?format=api) |
| [Get Launch](actions/get-launch.md) | `GET launches/{{id}}/` | [docs](https://ll.thespacedevs.com/2.3.0/launches/e3df2ecd-c239-472f-95e4-2b89b4f75800/?format=api) |
| [Get Space Station](actions/get-space-station.md) | `GET space_stations/{{id}}/` | [docs](https://ll.thespacedevs.com/2.3.0/space_stations/?format=api) |
| [List Agencies](actions/list-agencies.md) | `GET agencies/` | [docs](https://ll.thespacedevs.com/2.3.0/agencies/?format=api) |
| [List Astronauts](actions/list-astronauts.md) | `GET astronauts/` | [docs](https://ll.thespacedevs.com/2.3.0/astronauts/?format=api) |
| [List Docking Events](actions/list-docking-events.md) | `GET docking_events/` | [docs](https://ll.thespacedevs.com/2.3.0/docking_events/?format=api) |
| [List Events](actions/list-events.md) | `GET events/` | [docs](https://ll.thespacedevs.com/2.3.0/events/?format=api) |
| [List Expeditions](actions/list-expeditions.md) | `GET expeditions/` | [docs](https://ll.thespacedevs.com/2.3.0/expeditions/?format=api) |
| [List Launcher Configurations](actions/list-launcher-configurations.md) | `GET launcher_configurations/` | [docs](https://ll.thespacedevs.com/2.3.0/launcher_configurations/?format=api) |
| [List Launches](actions/list-launches.md) | `GET launches/` | [docs](https://ll.thespacedevs.com/2.3.0/launches/?format=api) |
| [List Locations](actions/list-locations.md) | `GET locations/` | [docs](https://ll.thespacedevs.com/2.3.0/locations/?format=api) |
| [List Pads](actions/list-pads.md) | `GET pads/` | [docs](https://ll.thespacedevs.com/2.3.0/pads/?format=api) |
| [List Payloads](actions/list-payloads.md) | `GET payloads/` | [docs](https://ll.thespacedevs.com/2.3.0/payloads/?format=api) |
| [List Previous Events](actions/list-previous-events.md) | `GET events/previous/` | [docs](https://ll.thespacedevs.com/2.3.0/events/previous/?format=api) |
| [List Previous Launches](actions/list-previous-launches.md) | `GET launches/previous/` | [docs](https://ll.thespacedevs.com/2.3.0/launches/previous/?format=api) |
| [List Programs](actions/list-programs.md) | `GET programs/` | [docs](https://ll.thespacedevs.com/2.3.0/programs/?format=api) |
| [List Space Stations](actions/list-space-stations.md) | `GET space_stations/` | [docs](https://ll.thespacedevs.com/2.3.0/space_stations/?format=api) |
| [List Spacecraft](actions/list-spacecraft.md) | `GET spacecraft/` | [docs](https://ll.thespacedevs.com/2.3.0/spacecraft/?format=api) |
| [List Spacewalks](actions/list-spacewalks.md) | `GET spacewalks/` | [docs](https://ll.thespacedevs.com/2.3.0/spacewalks/?format=api) |
| [List Upcoming Events](actions/list-upcoming-events.md) | `GET events/upcoming/` | [docs](https://ll.thespacedevs.com/2.3.0/events/upcoming/?format=api) |
| [List Upcoming Launches](actions/list-upcoming-launches.md) | `GET launches/upcoming/` | [docs](https://ll.thespacedevs.com/2.3.0/launches/upcoming/?format=api) |
| [List Updates](actions/list-updates.md) | `GET updates/` | [docs](https://ll.thespacedevs.com/2.3.0/updates/?format=api) |
