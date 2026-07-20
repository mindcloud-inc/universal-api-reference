# Paradym Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Paradym expects, and each action page lists the fields available to sort.

## Paradym actions that support sorting

- [List Certificates](actions/list-certificates.md)
- [List DIDs](actions/list-dids.md)
- [List Issued Credentials](actions/list-issued-credentials.md)
- [List Mdoc Credential Templates](actions/list-mdoc-credential-templates.md)
- [List Presentation Templates](actions/list-presentation-templates.md)
- [List Project Members](actions/list-project-members.md)
- [List Projects](actions/list-projects.md)
- [List Sd-Jwt Vc Credential Templates](actions/list-sd-jwt-vc-credential-templates.md)
- [List Trusted Entities](actions/list-trusted-entities.md)
- [List Webhooks](actions/list-webhooks.md)
