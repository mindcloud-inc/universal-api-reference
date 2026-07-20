# Qive Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Qive expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Qive actions that support filtering

- [List Authorized CTes](actions/list-authorized-ctes.md)
- [List Authorized NFes](actions/list-authorized-nfes.md)
- [List CTe Events](actions/list-cte-events.md)
- [List CTe Events V2](actions/list-cte-events-v2.md)
- [List CTe-OS Events](actions/list-cte-os-events.md)
- [List Emitted NFes](actions/list-emitted-nfes.md)
- [List Emitted NFSes](actions/list-emitted-nfses.md)
- [List NFe Events V2](actions/list-nfe-events-v2.md)
- [List NFe Manifests](actions/list-nfe-manifests.md)
- [List NFe Manifests V2](actions/list-nfe-manifests-v2.md)
- [List NFSe Events](actions/list-nfse-events.md)
- [List Not-Taker CTe-OS](actions/list-not-taker-cte-os.md)
- [List Not-Taker CTes](actions/list-not-taker-ctes.md)
- [List Received NFes](actions/list-received-nfes.md)
- [List Received NFSes](actions/list-received-nfses.md)
- [List Received NFSes V2](actions/list-received-nfses-v2.md)
- [List Taker CTe-OS](actions/list-taker-cte-os.md)
- [List Taker CTes](actions/list-taker-ctes.md)
- [List Transporter NFes](actions/list-transporter-nfes.md)
