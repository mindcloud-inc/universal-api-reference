# Microsoft Teams Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Microsoft Teams expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Microsoft Teams actions that support filtering

- [List All Team Channels](actions/list-all-team-channels.md)
- [List Channel Tabs](actions/list-channel-tabs.md)
- [List Chats](actions/list-chats.md)
- [List Team Channels](actions/list-team-channels.md)
- [List Team Installed Apps](actions/list-team-installed-apps.md)
