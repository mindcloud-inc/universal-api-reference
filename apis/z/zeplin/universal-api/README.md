# <img src="https://images.mindcloud.co/apps/icons/716ae55a149ff63038853cb19d0c17676d406676-1200x600_1775141441515.jpeg" alt="Zeplin logo" width="28" height="28"> Zeplin: Universal API

Manage Zeplin screens, notes, annotations, projects, and design system data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zeplin/latest
- **Actions:** 121
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zeplin.io
- **Vendor API docs:** https://docs.zeplin.dev/reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (121)

### Color

| Action | Method | Description |
| --- | --- | --- |
| [List Project Colors](actions/list-project-colors.md) | GET | Retrieves a list of project colors from Zeplin. |
| [List Styleguide Colors](actions/list-styleguide-colors.md) | GET | Retrieves a list of styleguide colors from Zeplin. |

### Component

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Component](actions/get-project-component.md) | GET | Retrieves a project component from Zeplin. |
| [Get Styleguide Component](actions/get-styleguide-component.md) | GET | Retrieves a styleguide component from Zeplin. |
| [List Project Components](actions/list-project-components.md) | GET | Retrieves a list of project components from Zeplin. |
| [List Screen Components](actions/list-screen-components.md) | GET | Retrieves a list of screen components from Zeplin. |
| [List Styleguide Components](actions/list-styleguide-components.md) | GET | Retrieves a list of styleguide components from Zeplin. |

### Component Section

| Action | Method | Description |
| --- | --- | --- |
| [List Project Component Sections](actions/list-project-component-sections.md) | GET | Retrieves a list of project component sections from Zeplin. |
| [List Styleguide Component Sections](actions/list-styleguide-component-sections.md) | GET | Retrieves a list of styleguide component sections from Zeplin. |

### Component Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Component Latest Version](actions/get-project-component-latest-version.md) | GET | Retrieves the latest project component version from Zeplin. |
| [Get Styleguide Component Latest Version](actions/get-styleguide-component-latest-version.md) | GET | Retrieves the latest styleguide component version from Zeplin. |

### Connected Component

| Action | Method | Description |
| --- | --- | --- |
| [List Project Connected Components](actions/list-project-connected-components.md) | GET | Retrieves a list of project connected components from Zeplin. |
| [List Styleguide Connected Components](actions/list-styleguide-connected-components.md) | GET | Retrieves a list of styleguide connected components from Zeplin. |

### Design Tokens

| Action | Method | Description |
| --- | --- | --- |
| [List Project Design Tokens](actions/list-project-design-tokens.md) | GET | Retrieves a list of project design tokens from Zeplin. |
| [List Styleguide Design Tokens](actions/list-styleguide-design-tokens.md) | GET | Retrieves a list of styleguide design tokens from Zeplin. |

### Flow Board

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Flow Board](actions/get-project-flow-board.md) | GET | Retrieves a project flow board from Zeplin. |
| [List Project Flow Boards](actions/list-project-flow-boards.md) | GET | Retrieves a list of project flow boards from Zeplin. |

### Flow Board Connector

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Flow Board Connector](actions/get-project-flow-board-connector.md) | GET | Retrieves a project flow board connector from Zeplin. |
| [List Project Flow Board Connectors](actions/list-project-flow-board-connectors.md) | GET | Retrieves a list of project flow board connectors from Zeplin. |

### Flow Board Group

| Action | Method | Description |
| --- | --- | --- |
| [List Project Flow Board Groups](actions/list-project-flow-board-groups.md) | GET | Retrieves a list of project flow board groups from Zeplin. |

### Flow Board Node

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Flow Board Node](actions/get-project-flow-board-node.md) | GET | Retrieves a project flow board node from Zeplin. |
| [List Project Flow Board Nodes](actions/list-project-flow-board-nodes.md) | GET | Retrieves a list of project flow board nodes from Zeplin. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Get User Notification](actions/get-user-notification.md) | GET | Retrieves an user notification from Zeplin. |
| [List User Notifications](actions/list-user-notifications.md) | GET | Retrieves a list of user notifications from Zeplin. |

### Object Reference

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization Webhook](actions/create-organization-webhook.md) | POST | Creates a new organization webhook in Zeplin. |
| [Create Project Color](actions/create-project-color.md) | POST | Creates a new project color in Zeplin. |
| [Create Project Webhook](actions/create-project-webhook.md) | POST | Creates a new project webhook in Zeplin. |
| [Create Screen](actions/create-screen.md) | POST | Creates a new screen in Zeplin. |
| [Create Screen Annotation](actions/create-screen-annotation.md) | POST | Creates a new screen annotation in Zeplin. |
| [Create Screen Comment](actions/create-screen-comment.md) | POST | Creates a new screen comment in Zeplin. |
| [Create Screen Note](actions/create-screen-note.md) | POST | Creates a new screen note in Zeplin. |
| [Create Screen Version](actions/create-screen-version.md) | POST | Creates a new screen version in Zeplin. |
| [Create Styleguide Color](actions/create-styleguide-color.md) | POST | Creates a new styleguide color in Zeplin. |
| [Create Styleguide Webhook](actions/create-styleguide-webhook.md) | POST | Creates a new styleguide webhook in Zeplin. |
| [Create User Webhook](actions/create-user-webhook.md) | POST | Creates a new user webhook in Zeplin. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Zeplin. |

### Organization Billing Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Billing](actions/get-organization-billing.md) | GET | Retrieves organization billing details from Zeplin. |

### Organization Member

| Action | Method | Description |
| --- | --- | --- |
| [Invite Organization Member](actions/invite-organization-member.md) | POST | Invites a member to a Zeplin organization. |
| [List Organization Members](actions/list-organization-members.md) | GET | Retrieves a list of organization members from Zeplin. |
| [Remove Organization Member](actions/remove-organization-member.md) | DELETE | Removes a member from a Zeplin organization. |
| [Update Organization Member](actions/update-organization-member.md) | PUT | Updates an existing organization member in Zeplin. |

### Organization Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves a list of organizations from Zeplin. |

### Organization Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Delete Organization Webhook](actions/delete-organization-webhook.md) | DELETE | Deletes an existing organization webhook from Zeplin. |
| [Get Organization Webhook](actions/get-organization-webhook.md) | GET | Retrieves an organization webhook from Zeplin. |
| [List Organization Webhooks](actions/list-organization-webhooks.md) | GET | Retrieves a list of organization webhooks from Zeplin. |
| [Update Organization Webhook](actions/update-organization-webhook.md) | PUT | Updates an existing organization webhook in Zeplin. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [List Project Pages](actions/list-project-pages.md) | GET | Retrieves a list of project pages from Zeplin. |
| [List Styleguide Pages](actions/list-styleguide-pages.md) | GET | Retrieves a list of styleguide pages from Zeplin. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Zeplin. |
| [List Organization Member Projects](actions/list-organization-member-projects.md) | GET | Retrieves a list of organization member projects from Zeplin. |
| [List Organization Projects](actions/list-organization-projects.md) | GET | Retrieves a list of organization projects from Zeplin. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Zeplin. |
| [List Styleguide Linked Projects](actions/list-styleguide-linked-projects.md) | GET | Retrieves a list of styleguide linked projects from Zeplin. |
| [List User Projects](actions/list-user-projects.md) | GET | Retrieves a list of user projects from Zeplin. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Zeplin. |

### Project Color

| Action | Method | Description |
| --- | --- | --- |
| [Update Project Color](actions/update-project-color.md) | PUT | Updates an existing project color in Zeplin. |

### Project Component

| Action | Method | Description |
| --- | --- | --- |
| [Update Project Component](actions/update-project-component.md) | PUT | Updates an existing project component in Zeplin. |

### Project Member

| Action | Method | Description |
| --- | --- | --- |
| [Invite Project Member](actions/invite-project-member.md) | POST | Invites a member to a Zeplin project. |
| [List Project Members](actions/list-project-members.md) | GET | Retrieves a list of project members from Zeplin. |
| [Remove Project Member](actions/remove-project-member.md) | DELETE | Removes a member from a Zeplin project. |

### Project Spacing Token

| Action | Method | Description |
| --- | --- | --- |
| [Update Project Spacing Token](actions/update-project-spacing-token.md) | PUT | Updates an existing project spacing token in Zeplin. |

### Project Text Style

| Action | Method | Description |
| --- | --- | --- |
| [Update Project Text Style](actions/update-project-text-style.md) | PUT | Updates an existing project text style in Zeplin. |

### Project Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project Webhook](actions/delete-project-webhook.md) | DELETE | Deletes an existing project webhook from Zeplin. |
| [Get Project Webhook](actions/get-project-webhook.md) | GET | Retrieves a project webhook from Zeplin. |
| [List Project Webhooks](actions/list-project-webhooks.md) | GET | Retrieves a list of project webhooks from Zeplin. |
| [Update Project Webhook](actions/update-project-webhook.md) | PUT | Updates an existing project webhook in Zeplin. |

### Screen

| Action | Method | Description |
| --- | --- | --- |
| [Get Screen](actions/get-screen.md) | GET | Retrieves a screen from Zeplin. |
| [List Project Screens](actions/list-project-screens.md) | GET | Retrieves a list of project screens from Zeplin. |
| [Update Screen](actions/update-screen.md) | PUT | Updates an existing screen in Zeplin. |

### Screen Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Delete Screen Annotation](actions/delete-screen-annotation.md) | DELETE | Deletes an existing screen annotation from Zeplin. |
| [Get Screen Annotation](actions/get-screen-annotation.md) | GET | Retrieves a screen annotation from Zeplin. |
| [List Screen Annotations](actions/list-screen-annotations.md) | GET | Retrieves a list of screen annotations from Zeplin. |
| [Update Screen Annotation](actions/update-screen-annotation.md) | PUT | Updates an existing screen annotation in Zeplin. |

### Screen Annotation Note Type

| Action | Method | Description |
| --- | --- | --- |
| [List Screen Annotation Note Types](actions/list-screen-annotation-note-types.md) | GET | Retrieves screen annotation note types from Zeplin. |

### Screen Comment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Screen Comment](actions/delete-screen-comment.md) | DELETE | Deletes an existing screen comment from Zeplin. |
| [Update Screen Comment](actions/update-screen-comment.md) | PUT | Updates an existing screen comment in Zeplin. |

### Screen Note

| Action | Method | Description |
| --- | --- | --- |
| [Delete Screen Note](actions/delete-screen-note.md) | DELETE | Deletes an existing screen note from Zeplin. |
| [Get Screen Note](actions/get-screen-note.md) | GET | Retrieves a screen note from Zeplin. |
| [List Screen Notes](actions/list-screen-notes.md) | GET | Retrieves a list of screen notes from Zeplin. |
| [Update Screen Note](actions/update-screen-note.md) | PUT | Updates an existing screen note in Zeplin. |

### Screen Section

| Action | Method | Description |
| --- | --- | --- |
| [Get Screen Section](actions/get-screen-section.md) | GET | Retrieves a screen section from Zeplin. |
| [List Screen Sections](actions/list-screen-sections.md) | GET | Retrieves a list of screen sections from Zeplin. |

### Screen Variant Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Screen Variant](actions/get-screen-variant.md) | GET | Retrieves a screen variant from Zeplin. |
| [List Screen Variants](actions/list-screen-variants.md) | GET | Retrieves a list of screen variants from Zeplin. |

### Screen Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Screen Version](actions/get-latest-screen-version.md) | GET | Retrieves the latest screen version from Zeplin. |
| [Get Screen Version](actions/get-screen-version.md) | GET | Retrieves a screen version from Zeplin. |

### Screen Version Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Screen Versions](actions/list-screen-versions.md) | GET | Retrieves a list of screen versions from Zeplin. |

### Spacing Section

| Action | Method | Description |
| --- | --- | --- |
| [List Project Spacing Sections](actions/list-project-spacing-sections.md) | GET | Retrieves a list of project spacing sections from Zeplin. |
| [List Styleguide Spacing Sections](actions/list-styleguide-spacing-sections.md) | GET | Retrieves a list of styleguide spacing sections from Zeplin. |

### Spacing Token

| Action | Method | Description |
| --- | --- | --- |
| [List Project Spacing Tokens](actions/list-project-spacing-tokens.md) | GET | Retrieves a list of project spacing tokens from Zeplin. |
| [List Styleguide Spacing Tokens](actions/list-styleguide-spacing-tokens.md) | GET | Retrieves a list of styleguide spacing tokens from Zeplin. |

### Styleguide

| Action | Method | Description |
| --- | --- | --- |
| [Get Styleguide](actions/get-styleguide.md) | GET | Retrieves a styleguide from Zeplin. |
| [List Organization Member Styleguides](actions/list-organization-member-styleguides.md) | GET | Retrieves a list of organization member styleguides from Zeplin. |
| [List Organization Styleguides](actions/list-organization-styleguides.md) | GET | Retrieves a list of organization styleguides from Zeplin. |
| [List Styleguides](actions/list-styleguides.md) | GET | Retrieves a list of styleguides from Zeplin. |
| [List User Styleguides](actions/list-user-styleguides.md) | GET | Retrieves a list of user styleguides from Zeplin. |
| [Update Styleguide](actions/update-styleguide.md) | PUT | Updates an existing styleguide in Zeplin. |

### Styleguide Color

| Action | Method | Description |
| --- | --- | --- |
| [Update Styleguide Color](actions/update-styleguide-color.md) | PUT | Updates an existing styleguide color in Zeplin. |

### Styleguide Component

| Action | Method | Description |
| --- | --- | --- |
| [Update Styleguide Component](actions/update-styleguide-component.md) | PUT | Updates an existing styleguide component in Zeplin. |

### Styleguide Member

| Action | Method | Description |
| --- | --- | --- |
| [Invite Styleguide Member](actions/invite-styleguide-member.md) | POST | Invites a member to a Zeplin styleguide. |
| [List Styleguide Members](actions/list-styleguide-members.md) | GET | Retrieves a list of styleguide members from Zeplin. |
| [Remove Styleguide Member](actions/remove-styleguide-member.md) | DELETE | Removes a member from a Zeplin styleguide. |

### Styleguide Spacing Token

| Action | Method | Description |
| --- | --- | --- |
| [Update Styleguide Spacing Token](actions/update-styleguide-spacing-token.md) | PUT | Updates an existing styleguide spacing token in Zeplin. |

### Styleguide Text Style

| Action | Method | Description |
| --- | --- | --- |
| [Update Styleguide Text Style](actions/update-styleguide-text-style.md) | PUT | Updates an existing styleguide text style in Zeplin. |

### Styleguide Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Delete Styleguide Webhook](actions/delete-styleguide-webhook.md) | DELETE | Deletes an existing styleguide webhook from Zeplin. |
| [Get Styleguide Webhook](actions/get-styleguide-webhook.md) | GET | Retrieves a styleguide webhook from Zeplin. |
| [List Styleguide Webhooks](actions/list-styleguide-webhooks.md) | GET | Retrieves a list of styleguide webhooks from Zeplin. |
| [Update Styleguide Webhook](actions/update-styleguide-webhook.md) | PUT | Updates an existing styleguide webhook in Zeplin. |

### Text Style

| Action | Method | Description |
| --- | --- | --- |
| [List Project Text Styles](actions/list-project-text-styles.md) | GET | Retrieves a list of project text styles from Zeplin. |
| [List Styleguide Text Styles](actions/list-styleguide-text-styles.md) | GET | Retrieves a list of styleguide text styles from Zeplin. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Zeplin. |
| [List Organization Aliens](actions/list-organization-aliens.md) | GET | Retrieves a list of organization aliens from Zeplin. |

### User Notification

| Action | Method | Description |
| --- | --- | --- |
| [Update User Notification](actions/update-user-notification.md) | PUT | Updates an existing user notification in Zeplin. |
| [Update User Notification Settings](actions/update-user-notification-settings.md) | PUT | Updates user notification settings in Zeplin. |

### User Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Delete User Webhook](actions/delete-user-webhook.md) | DELETE | Deletes an existing user webhook from Zeplin. |
| [Get User Webhook](actions/get-user-webhook.md) | GET | Retrieves an user webhook from Zeplin. |
| [List User Webhooks](actions/list-user-webhooks.md) | GET | Retrieves a list of user webhooks from Zeplin. |
| [Update User Webhook](actions/update-user-webhook.md) | PUT | Updates an existing user webhook in Zeplin. |

### Variable Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Project Variable Collections](actions/list-project-variable-collections.md) | GET | Retrieves a list of project variable collections from Zeplin. |
| [List Styleguide Variable Collections](actions/list-styleguide-variable-collections.md) | GET | Retrieves a list of styleguide variable collections from Zeplin. |

### Workflow Status

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Workflow Statuses](actions/list-organization-workflow-statuses.md) | GET | Retrieves a list of organization workflow statuses from Zeplin. |

