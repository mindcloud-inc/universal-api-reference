# Zeplin Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zeplin expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-member-projects?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string&memberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zeplin actions that support pagination

- [List Organization Member Projects](actions/list-organization-member-projects.md)
- [List Organization Member Styleguides](actions/list-organization-member-styleguides.md)
- [List Organization Members](actions/list-organization-members.md)
- [List Organization Projects](actions/list-organization-projects.md)
- [List Organization Styleguides](actions/list-organization-styleguides.md)
- [List Organization Webhooks](actions/list-organization-webhooks.md)
- [List Project Colors](actions/list-project-colors.md)
- [List Project Component Sections](actions/list-project-component-sections.md)
- [List Project Components](actions/list-project-components.md)
- [List Project Connected Components](actions/list-project-connected-components.md)
- [List Project Flow Board Connectors](actions/list-project-flow-board-connectors.md)
- [List Project Flow Board Nodes](actions/list-project-flow-board-nodes.md)
- [List Project Members](actions/list-project-members.md)
- [List Project Pages](actions/list-project-pages.md)
- [List Project Screens](actions/list-project-screens.md)
- [List Project Spacing Sections](actions/list-project-spacing-sections.md)
- [List Project Spacing Tokens](actions/list-project-spacing-tokens.md)
- [List Project Text Styles](actions/list-project-text-styles.md)
- [List Project Variable Collections](actions/list-project-variable-collections.md)
- [List Project Webhooks](actions/list-project-webhooks.md)
- [List Projects](actions/list-projects.md)
- [List Screen Annotations](actions/list-screen-annotations.md)
- [List Screen Components](actions/list-screen-components.md)
- [List Screen Notes](actions/list-screen-notes.md)
- [List Screen Sections](actions/list-screen-sections.md)
- [List Screen Variants](actions/list-screen-variants.md)
- [List Screen Versions](actions/list-screen-versions.md)
- [List Styleguide Colors](actions/list-styleguide-colors.md)
- [List Styleguide Component Sections](actions/list-styleguide-component-sections.md)
- [List Styleguide Components](actions/list-styleguide-components.md)
- [List Styleguide Connected Components](actions/list-styleguide-connected-components.md)
- [List Styleguide Linked Projects](actions/list-styleguide-linked-projects.md)
- [List Styleguide Members](actions/list-styleguide-members.md)
- [List Styleguide Pages](actions/list-styleguide-pages.md)
- [List Styleguide Spacing Sections](actions/list-styleguide-spacing-sections.md)
- [List Styleguide Spacing Tokens](actions/list-styleguide-spacing-tokens.md)
- [List Styleguide Text Styles](actions/list-styleguide-text-styles.md)
- [List Styleguide Variable Collections](actions/list-styleguide-variable-collections.md)
- [List Styleguide Webhooks](actions/list-styleguide-webhooks.md)
- [List Styleguides](actions/list-styleguides.md)
- [List User Notifications](actions/list-user-notifications.md)
- [List User Projects](actions/list-user-projects.md)
- [List User Styleguides](actions/list-user-styleguides.md)
- [List User Webhooks](actions/list-user-webhooks.md)
