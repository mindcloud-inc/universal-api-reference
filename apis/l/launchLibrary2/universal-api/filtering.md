# Launch Library 2 Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Launch Library 2 expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Launch Library 2 actions that support filtering

- [List Agencies](actions/list-agencies.md)
- [List Astronauts](actions/list-astronauts.md)
- [List Docking Events](actions/list-docking-events.md)
- [List Events](actions/list-events.md)
- [List Expeditions](actions/list-expeditions.md)
- [List Launcher Configurations](actions/list-launcher-configurations.md)
- [List Launches](actions/list-launches.md)
- [List Locations](actions/list-locations.md)
- [List Pads](actions/list-pads.md)
- [List Payloads](actions/list-payloads.md)
- [List Previous Events](actions/list-previous-events.md)
- [List Previous Launches](actions/list-previous-launches.md)
- [List Programs](actions/list-programs.md)
- [List Space Stations](actions/list-space-stations.md)
- [List Spacecraft](actions/list-spacecraft.md)
- [List Spacewalks](actions/list-spacewalks.md)
- [List Upcoming Events](actions/list-upcoming-events.md)
- [List Upcoming Launches](actions/list-upcoming-launches.md)
- [List Updates](actions/list-updates.md)
