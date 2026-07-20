# Zeplin: Native API Reference

A consolidated summary of Zeplin's API configuration and 121 documented operations, with links to official documentation.

- **Official docs:** https://docs.zeplin.dev/reference/introduction
- **API base URL:** `https://api.zeplin.dev/v1`

## Authentication

### OAuth2

Connect a Zeplin account with OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.zeplin.dev/v1/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.zeplin.dev/v1/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.zeplin.dev/v1/oauth/token.

[Official authentication documentation](https://docs.zeplin.dev/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 30; maximum 100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (121 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Organization Webhook](actions/create-organization-webhook.md) | `POST /organizations/{organization_id}/webhooks` | [docs](https://docs.zeplin.dev/reference/createorganizationwebhooks) |
| [Create Project Color](actions/create-project-color.md) | `POST /projects/{project_id}/colors` | [docs](https://docs.zeplin.dev/reference/createprojectcolor) |
| [Create Project Webhook](actions/create-project-webhook.md) | `POST /projects/{project_id}/webhooks` | [docs](https://docs.zeplin.dev/reference/createprojectwebhooks) |
| [Create Screen](actions/create-screen.md) | `POST /projects/{project_id}/screens` | [docs](https://docs.zeplin.dev/reference/createscreen) |
| [Create Screen Annotation](actions/create-screen-annotation.md) | `POST /projects/{project_id}/screens/{screen_id}/annotations` | [docs](https://docs.zeplin.dev/reference/createscreenannotation) |
| [Create Screen Comment](actions/create-screen-comment.md) | `POST /projects/{project_id}/screens/{screen_id}/notes/{note_id}/comments` | [docs](https://docs.zeplin.dev/reference/createscreencomment) |
| [Create Screen Note](actions/create-screen-note.md) | `POST /projects/{project_id}/screens/{screen_id}/notes` | [docs](https://docs.zeplin.dev/reference/createscreennote) |
| [Create Screen Version](actions/create-screen-version.md) | `POST /projects/{project_id}/screens/{screen_id}/versions` | [docs](https://docs.zeplin.dev/reference/createscreenversion) |
| [Create Styleguide Color](actions/create-styleguide-color.md) | `POST /styleguides/{styleguide_id}/colors` | [docs](https://docs.zeplin.dev/reference/createstyleguidecolor) |
| [Create Styleguide Webhook](actions/create-styleguide-webhook.md) | `POST /styleguides/{styleguide_id}/webhooks` | [docs](https://docs.zeplin.dev/reference/createstyleguidewebhooks) |
| [Create User Webhook](actions/create-user-webhook.md) | `POST /users/me/webhooks` | [docs](https://docs.zeplin.dev/reference/createuserwebhooks) |
| [Delete Organization Webhook](actions/delete-organization-webhook.md) | `DELETE /organizations/{organization_id}/webhooks/{webhook_id}` | [docs](https://docs.zeplin.dev/reference/deleteorganizationwebhook) |
| [Delete Project Webhook](actions/delete-project-webhook.md) | `DELETE /projects/{project_id}/webhooks/{webhook_id}` | [docs](https://docs.zeplin.dev/reference/deleteprojectwebhook) |
| [Delete Screen Annotation](actions/delete-screen-annotation.md) | `DELETE /projects/{project_id}/screens/{screen_id}/annotations/{annotation_id}` | [docs](https://docs.zeplin.dev/reference/deletescreenannotation) |
| [Delete Screen Comment](actions/delete-screen-comment.md) | `DELETE /projects/{project_id}/screens/{screen_id}/notes/{note_id}/comments/{comment_id}` | [docs](https://docs.zeplin.dev/reference/deletescreencomment) |
| [Delete Screen Note](actions/delete-screen-note.md) | `DELETE /projects/{project_id}/screens/{screen_id}/notes/{note_id}` | [docs](https://docs.zeplin.dev/reference/deletescreennote) |
| [Delete Styleguide Webhook](actions/delete-styleguide-webhook.md) | `DELETE /styleguides/{styleguide_id}/webhooks/{webhook_id}` | [docs](https://docs.zeplin.dev/reference/deletestyleguidewebhook) |
| [Delete User Webhook](actions/delete-user-webhook.md) | `DELETE /users/me/webhooks/{webhook_id}` | [docs](https://docs.zeplin.dev/reference/deleteuserwebhook) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://docs.zeplin.dev/reference/getcurrentuser) |
| [Get Latest Screen Version](actions/get-latest-screen-version.md) | `GET /projects/{project_id}/screens/{screen_id}/versions/latest` | [docs](https://docs.zeplin.dev/reference/getlatestscreenversion) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/{organization_id}` | [docs](https://docs.zeplin.dev/reference/getorganization) |
| [Get Organization Billing](actions/get-organization-billing.md) | `GET /organizations/{organization_id}/billing` | [docs](https://docs.zeplin.dev/reference/getorganizationbilling) |
| [Get Organization Webhook](actions/get-organization-webhook.md) | `GET /organizations/{organization_id}/webhooks/{webhook_id}` | [docs](https://docs.zeplin.dev/reference/getorganizationwebhook) |
| [Get Project](actions/get-project.md) | `GET /projects/{project_id}` | [docs](https://docs.zeplin.dev/reference/getproject) |
| [Get Project Component](actions/get-project-component.md) | `GET /projects/{project_id}/components/{component_id}` | [docs](https://docs.zeplin.dev/reference/getprojectcomponent) |
| [Get Project Component Latest Version](actions/get-project-component-latest-version.md) | `GET /projects/{project_id}/components/{component_id}/versions/latest` | [docs](https://docs.zeplin.dev/reference/getprojectcomponentlatestversion) |
| [Get Project Flow Board](actions/get-project-flow-board.md) | `GET /projects/{project_id}/flow_boards/{flow_board_id}` | [docs](https://docs.zeplin.dev/reference/getprojectflowboard) |
| [Get Project Flow Board Connector](actions/get-project-flow-board-connector.md) | `GET /projects/{project_id}/flow_boards/{flow_board_id}/connectors/{connector_id}` | [docs](https://docs.zeplin.dev/reference/getprojectflowboardconnector) |
| [Get Project Flow Board Node](actions/get-project-flow-board-node.md) | `GET /projects/{project_id}/flow_boards/{flow_board_id}/nodes/{node_id}` | [docs](https://docs.zeplin.dev/reference/getprojectflowboardnode) |
| [Get Project Webhook](actions/get-project-webhook.md) | `GET /projects/{project_id}/webhooks/{webhook_id}` | [docs](https://docs.zeplin.dev/reference/getprojectwebhook) |
| [Get Screen](actions/get-screen.md) | `GET /projects/{project_id}/screens/{screen_id}` | [docs](https://docs.zeplin.dev/reference/getscreen) |
| [Get Screen Annotation](actions/get-screen-annotation.md) | `GET /projects/{project_id}/screens/{screen_id}/annotations/{annotation_id}` | [docs](https://docs.zeplin.dev/reference/getscreenannotation) |
| [Get Screen Note](actions/get-screen-note.md) | `GET /projects/{project_id}/screens/{screen_id}/notes/{note_id}` | [docs](https://docs.zeplin.dev/reference/getscreennote) |
| [Get Screen Section](actions/get-screen-section.md) | `GET /projects/{project_id}/screen_sections/{section_id}` | [docs](https://docs.zeplin.dev/reference/getscreensection) |
| [Get Screen Variant](actions/get-screen-variant.md) | `GET /projects/{project_id}/screen_variants/{variant_id}` | [docs](https://docs.zeplin.dev/reference/getscreenvariant) |
| [Get Screen Version](actions/get-screen-version.md) | `GET /projects/{project_id}/screens/{screen_id}/versions/{version_id}` | [docs](https://docs.zeplin.dev/reference/getscreenversion) |
| [Get Styleguide](actions/get-styleguide.md) | `GET /styleguides/{styleguide_id}` | [docs](https://docs.zeplin.dev/reference/getstyleguide) |
| [Get Styleguide Component](actions/get-styleguide-component.md) | `GET /styleguides/{styleguide_id}/components/{component_id}` | [docs](https://docs.zeplin.dev/reference/getstyleguidecomponent) |
| [Get Styleguide Component Latest Version](actions/get-styleguide-component-latest-version.md) | `GET /styleguides/{styleguide_id}/components/{component_id}/versions/latest` | [docs](https://docs.zeplin.dev/reference/getstyleguidecomponentlatestversion) |
| [Get Styleguide Webhook](actions/get-styleguide-webhook.md) | `GET /styleguides/{styleguide_id}/webhooks/{webhook_id}` | [docs](https://docs.zeplin.dev/reference/getstyleguidewebhook) |
| [Get User Notification](actions/get-user-notification.md) | `GET /users/me/notifications/{notification_id}` | [docs](https://docs.zeplin.dev/reference/getusernotification) |
| [Get User Webhook](actions/get-user-webhook.md) | `GET /users/me/webhooks/{webhook_id}` | [docs](https://docs.zeplin.dev/reference/getuserwebhook) |
| [Invite Organization Member](actions/invite-organization-member.md) | `POST /organizations/{organization_id}/members` | [docs](https://docs.zeplin.dev/reference/inviteorganizationmember) |
| [Invite Project Member](actions/invite-project-member.md) | `POST /projects/{project_id}/members` | [docs](https://docs.zeplin.dev/reference/inviteprojectmember) |
| [Invite Styleguide Member](actions/invite-styleguide-member.md) | `POST /styleguides/{styleguide_id}/members` | [docs](https://docs.zeplin.dev/reference/invitestyleguidemember) |
| [List Organization Aliens](actions/list-organization-aliens.md) | `GET /organizations/{organization_id}/aliens` | [docs](https://docs.zeplin.dev/reference/getorganizationaliens) |
| [List Organization Member Projects](actions/list-organization-member-projects.md) | `GET /organizations/{organization_id}/members/{member_id}/projects` | [docs](https://docs.zeplin.dev/reference/getorganizationmemberprojects) |
| [List Organization Member Styleguides](actions/list-organization-member-styleguides.md) | `GET /organizations/{organization_id}/members/{member_id}/styleguides` | [docs](https://docs.zeplin.dev/reference/getorganizationmemberstyleguides) |
| [List Organization Members](actions/list-organization-members.md) | `GET /organizations/{organization_id}/members` | [docs](https://docs.zeplin.dev/reference/getorganizationmembers) |
| [List Organization Projects](actions/list-organization-projects.md) | `GET /organizations/{organization_id}/projects` | [docs](https://docs.zeplin.dev/reference/getorganizationprojects) |
| [List Organization Styleguides](actions/list-organization-styleguides.md) | `GET /organizations/{organization_id}/styleguides` | [docs](https://docs.zeplin.dev/reference/getorganizationstyleguides) |
| [List Organization Webhooks](actions/list-organization-webhooks.md) | `GET /organizations/{organization_id}/webhooks` | [docs](https://docs.zeplin.dev/reference/getorganizationwebhooks) |
| [List Organization Workflow Statuses](actions/list-organization-workflow-statuses.md) | `GET /organizations/{organization_id}/workflow_statuses` | [docs](https://docs.zeplin.dev/reference/getorganizationworkflowstatuses) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://docs.zeplin.dev/reference/getorganizations) |
| [List Project Colors](actions/list-project-colors.md) | `GET /projects/{project_id}/colors` | [docs](https://docs.zeplin.dev/reference/getprojectcolors) |
| [List Project Component Sections](actions/list-project-component-sections.md) | `GET /projects/{project_id}/component_sections` | [docs](https://docs.zeplin.dev/reference/getprojectcomponentsections) |
| [List Project Components](actions/list-project-components.md) | `GET /projects/{project_id}/components` | [docs](https://docs.zeplin.dev/reference/getprojectcomponents) |
| [List Project Connected Components](actions/list-project-connected-components.md) | `GET /projects/{project_id}/connected_components` | [docs](https://docs.zeplin.dev/reference/getprojectconnectedcomponents) |
| [List Project Design Tokens](actions/list-project-design-tokens.md) | `GET /projects/{project_id}/design_tokens` | [docs](https://docs.zeplin.dev/reference/getprojectdesigntokens) |
| [List Project Flow Board Connectors](actions/list-project-flow-board-connectors.md) | `GET /projects/{project_id}/flow_boards/{flow_board_id}/connectors` | [docs](https://docs.zeplin.dev/reference/getprojectflowboardconnectors) |
| [List Project Flow Board Groups](actions/list-project-flow-board-groups.md) | `GET /projects/{project_id}/flow_boards/{flow_board_id}/groups` | [docs](https://docs.zeplin.dev/reference/getprojectflowboardgroups) |
| [List Project Flow Board Nodes](actions/list-project-flow-board-nodes.md) | `GET /projects/{project_id}/flow_boards/{flow_board_id}/nodes` | [docs](https://docs.zeplin.dev/reference/getprojectflowboardnodes) |
| [List Project Flow Boards](actions/list-project-flow-boards.md) | `GET /projects/{project_id}/flow_boards` | [docs](https://docs.zeplin.dev/reference/getprojectflowboards) |
| [List Project Members](actions/list-project-members.md) | `GET /projects/{project_id}/members` | [docs](https://docs.zeplin.dev/reference/getprojectmembers) |
| [List Project Pages](actions/list-project-pages.md) | `GET /projects/{project_id}/pages` | [docs](https://docs.zeplin.dev/reference/getprojectpages) |
| [List Project Screens](actions/list-project-screens.md) | `GET /projects/{project_id}/screens` | [docs](https://docs.zeplin.dev/reference/getprojectscreens) |
| [List Project Spacing Sections](actions/list-project-spacing-sections.md) | `GET /projects/{project_id}/spacing_sections` | [docs](https://docs.zeplin.dev/reference/getprojectspacingsections) |
| [List Project Spacing Tokens](actions/list-project-spacing-tokens.md) | `GET /projects/{project_id}/spacing_tokens` | [docs](https://docs.zeplin.dev/reference/getprojectspacingtokens) |
| [List Project Text Styles](actions/list-project-text-styles.md) | `GET /projects/{project_id}/text_styles` | [docs](https://docs.zeplin.dev/reference/getprojecttextstyles) |
| [List Project Variable Collections](actions/list-project-variable-collections.md) | `GET /projects/{project_id}/variable_collections` | [docs](https://docs.zeplin.dev/reference/getprojectvariablecollections) |
| [List Project Webhooks](actions/list-project-webhooks.md) | `GET /projects/{project_id}/webhooks` | [docs](https://docs.zeplin.dev/reference/getprojectwebhooks) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.zeplin.dev/reference/getprojects) |
| [List Screen Annotation Note Types](actions/list-screen-annotation-note-types.md) | `GET /projects/{project_id}/annotations/note_types` | [docs](https://docs.zeplin.dev/reference/getscreenannotationsnotetypes) |
| [List Screen Annotations](actions/list-screen-annotations.md) | `GET /projects/{project_id}/screens/{screen_id}/annotations` | [docs](https://docs.zeplin.dev/reference/getscreenannotations) |
| [List Screen Components](actions/list-screen-components.md) | `GET /projects/{project_id}/screens/{screen_id}/components` | [docs](https://docs.zeplin.dev/reference/getscreencomponents) |
| [List Screen Notes](actions/list-screen-notes.md) | `GET /projects/{project_id}/screens/{screen_id}/notes` | [docs](https://docs.zeplin.dev/reference/getscreennotes) |
| [List Screen Sections](actions/list-screen-sections.md) | `GET /projects/{project_id}/screen_sections` | [docs](https://docs.zeplin.dev/reference/getscreensections) |
| [List Screen Variants](actions/list-screen-variants.md) | `GET /projects/{project_id}/screen_variants` | [docs](https://docs.zeplin.dev/reference/getscreenvariants) |
| [List Screen Versions](actions/list-screen-versions.md) | `GET /projects/{project_id}/screens/{screen_id}/versions` | [docs](https://docs.zeplin.dev/reference/getscreenversions) |
| [List Styleguide Colors](actions/list-styleguide-colors.md) | `GET /styleguides/{styleguide_id}/colors` | [docs](https://docs.zeplin.dev/reference/getstyleguidecolors) |
| [List Styleguide Component Sections](actions/list-styleguide-component-sections.md) | `GET /styleguides/{styleguide_id}/component_sections` | [docs](https://docs.zeplin.dev/reference/getstyleguidecomponentsections) |
| [List Styleguide Components](actions/list-styleguide-components.md) | `GET /styleguides/{styleguide_id}/components` | [docs](https://docs.zeplin.dev/reference/getstyleguidecomponents) |
| [List Styleguide Connected Components](actions/list-styleguide-connected-components.md) | `GET /styleguides/{styleguide_id}/connected_components` | [docs](https://docs.zeplin.dev/reference/getstyleguideconnectedcomponents) |
| [List Styleguide Design Tokens](actions/list-styleguide-design-tokens.md) | `GET /styleguides/{styleguide_id}/design_tokens` | [docs](https://docs.zeplin.dev/reference/getstyleguidedesigntokens) |
| [List Styleguide Linked Projects](actions/list-styleguide-linked-projects.md) | `GET /styleguides/{styleguide_id}/linked_projects` | [docs](https://docs.zeplin.dev/reference/getstyleguidelinkedprojects) |
| [List Styleguide Members](actions/list-styleguide-members.md) | `GET /styleguides/{styleguide_id}/members` | [docs](https://docs.zeplin.dev/reference/getstyleguidemembers) |
| [List Styleguide Pages](actions/list-styleguide-pages.md) | `GET /styleguides/{styleguide_id}/pages` | [docs](https://docs.zeplin.dev/reference/getstyleguidepages) |
| [List Styleguide Spacing Sections](actions/list-styleguide-spacing-sections.md) | `GET /styleguides/{styleguide_id}/spacing_sections` | [docs](https://docs.zeplin.dev/reference/getstyleguidespacingsections) |
| [List Styleguide Spacing Tokens](actions/list-styleguide-spacing-tokens.md) | `GET /styleguides/{styleguide_id}/spacing_tokens` | [docs](https://docs.zeplin.dev/reference/getstyleguidespacingtokens) |
| [List Styleguide Text Styles](actions/list-styleguide-text-styles.md) | `GET /styleguides/{styleguide_id}/text_styles` | [docs](https://docs.zeplin.dev/reference/getstyleguidetextstyles) |
| [List Styleguide Variable Collections](actions/list-styleguide-variable-collections.md) | `GET /styleguides/{styleguide_id}/variable_collections` | [docs](https://docs.zeplin.dev/reference/getstyleguidevariablecollections) |
| [List Styleguide Webhooks](actions/list-styleguide-webhooks.md) | `GET /styleguides/{styleguide_id}/webhooks` | [docs](https://docs.zeplin.dev/reference/getstyleguidewebhooks) |
| [List Styleguides](actions/list-styleguides.md) | `GET /styleguides` | [docs](https://docs.zeplin.dev/reference/getstyleguides) |
| [List User Notifications](actions/list-user-notifications.md) | `GET /users/me/notifications` | [docs](https://docs.zeplin.dev/reference/getusernotifications) |
| [List User Projects](actions/list-user-projects.md) | `GET /users/me/projects` | [docs](https://docs.zeplin.dev/reference/getuserprojects) |
| [List User Styleguides](actions/list-user-styleguides.md) | `GET /users/me/styleguides` | [docs](https://docs.zeplin.dev/reference/getuserstyleguides) |
| [List User Webhooks](actions/list-user-webhooks.md) | `GET /users/me/webhooks` | [docs](https://docs.zeplin.dev/reference/getuserwebhooks) |
| [Remove Organization Member](actions/remove-organization-member.md) | `DELETE /organizations/{organization_id}/members/{member_id}` | [docs](https://docs.zeplin.dev/reference/removeorganizationmember) |
| [Remove Project Member](actions/remove-project-member.md) | `DELETE /projects/{project_id}/members/{member_id}` | [docs](https://docs.zeplin.dev/reference/removeprojectmember) |
| [Remove Styleguide Member](actions/remove-styleguide-member.md) | `DELETE /styleguides/{styleguide_id}/members/{member_id}` | [docs](https://docs.zeplin.dev/reference/removestyleguidemember) |
| [Update Organization Member](actions/update-organization-member.md) | `PATCH /organizations/{organization_id}/members/{member_id}` | [docs](https://docs.zeplin.dev/reference/updateorganizationmember) |
| [Update Organization Webhook](actions/update-organization-webhook.md) | `PATCH /organizations/{organization_id}/webhooks/{webhook_id}` | [docs](https://docs.zeplin.dev/reference/updateorganizationwebhooks) |
| [Update Project](actions/update-project.md) | `PATCH /projects/{project_id}` | [docs](https://docs.zeplin.dev/reference/updateproject) |
| [Update Project Color](actions/update-project-color.md) | `PATCH /projects/{project_id}/colors/{color_id}` | [docs](https://docs.zeplin.dev/reference/updateprojectcolor) |
| [Update Project Component](actions/update-project-component.md) | `PATCH /projects/{project_id}/components/{component_id}` | [docs](https://docs.zeplin.dev/reference/updateprojectcomponent) |
| [Update Project Spacing Token](actions/update-project-spacing-token.md) | `PATCH /projects/{project_id}/spacing_tokens/{spacing_token_id}` | [docs](https://docs.zeplin.dev/reference/updateprojectspacingtoken) |
| [Update Project Text Style](actions/update-project-text-style.md) | `PATCH /projects/{project_id}/text_styles/{text_style_id}` | [docs](https://docs.zeplin.dev/reference/updateprojecttextstyle) |
| [Update Project Webhook](actions/update-project-webhook.md) | `PATCH /projects/{project_id}/webhooks/{webhook_id}` | [docs](https://docs.zeplin.dev/reference/updateprojectwebhooks) |
| [Update Screen](actions/update-screen.md) | `PATCH /projects/{project_id}/screens/{screen_id}` | [docs](https://docs.zeplin.dev/reference/updatescreen) |
| [Update Screen Annotation](actions/update-screen-annotation.md) | `PATCH /projects/{project_id}/screens/{screen_id}/annotations/{annotation_id}` | [docs](https://docs.zeplin.dev/reference/updatescreenannotation) |
| [Update Screen Comment](actions/update-screen-comment.md) | `PATCH /projects/{project_id}/screens/{screen_id}/notes/{note_id}/comments/{comment_id}` | [docs](https://docs.zeplin.dev/reference/updatescreencomment) |
| [Update Screen Note](actions/update-screen-note.md) | `PATCH /projects/{project_id}/screens/{screen_id}/notes/{note_id}` | [docs](https://docs.zeplin.dev/reference/updatescreennote) |
| [Update Styleguide](actions/update-styleguide.md) | `PATCH /styleguides/{styleguide_id}` | [docs](https://docs.zeplin.dev/reference/updatestyleguide) |
| [Update Styleguide Color](actions/update-styleguide-color.md) | `PATCH /styleguides/{styleguide_id}/colors/{color_id}` | [docs](https://docs.zeplin.dev/reference/updatestyleguidecolor) |
| [Update Styleguide Component](actions/update-styleguide-component.md) | `PATCH /styleguides/{styleguide_id}/components/{component_id}` | [docs](https://docs.zeplin.dev/reference/updatestyleguidecomponent) |
| [Update Styleguide Spacing Token](actions/update-styleguide-spacing-token.md) | `PATCH /styleguides/{styleguide_id}/spacing_tokens/{spacing_token_id}` | [docs](https://docs.zeplin.dev/reference/updatestyleguidespacingtoken) |
| [Update Styleguide Text Style](actions/update-styleguide-text-style.md) | `PATCH /styleguides/{styleguide_id}/text_styles/{text_style_id}` | [docs](https://docs.zeplin.dev/reference/updatestyleguidetextstyle) |
| [Update Styleguide Webhook](actions/update-styleguide-webhook.md) | `PATCH /styleguides/{styleguide_id}/webhooks/{webhook_id}` | [docs](https://docs.zeplin.dev/reference/updatestyleguidewebhooks) |
| [Update User Notification](actions/update-user-notification.md) | `PATCH /users/me/notifications/{notification_id}` | [docs](https://docs.zeplin.dev/reference/updateusernotification) |
| [Update User Notification Settings](actions/update-user-notification-settings.md) | `PATCH /users/me/notifications` | [docs](https://docs.zeplin.dev/reference/updateusernotifications) |
| [Update User Webhook](actions/update-user-webhook.md) | `PATCH /users/me/webhooks/{webhook_id}` | [docs](https://docs.zeplin.dev/reference/updateuserwebhooks) |
