# Airslate: Native API Reference

A consolidated summary of Airslate's API configuration and 84 documented operations, with links to official documentation.

- **Official docs:** https://docs.airslate.io/docs/airslate-api/reference
- **API base URL:** `https://api.airslate.io/v1`

## Authentication

### OAuth2 Authorization Code

Authenticate against Airslate using the documented OAuth 2.0 authorization-code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://oauth.airslate.com/public/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth.airslate.com/public/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid email profile`.

Refresh expired access tokens with a POST request to https://oauth.airslate.com/public/oauth/token.

[Official authentication documentation](https://docs.airslate.io/docs/airslate-api/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (84 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Group Members](actions/add-group-members.md) | `POST /organizations/{organization_id}/groups/{group_id}/members` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [Add Template Tag](actions/add-template-tag.md) | `POST /organizations/{organization_id}/templates/{template_id}/tags` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Add Web Form Field](actions/add-web-form-field.md) | `POST /organizations/{organization_id}/templates/{template_id}/forms/{form_id}/fields` | [docs](https://docs.airslate.io/docs/airslate-api/forms-api) |
| [Attach Template Bot](actions/attach-template-bot.md) | `POST /organizations/{organization_id}/templates/{template_id}/bots` | [docs](https://docs.airslate.io/docs/airslate-api/bots-api) |
| [Cancel Organization User Invite](actions/cancel-organization-user-invite.md) | `DELETE /organizations/{organization_id}/users/{user_id}/reject-invite` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [Create Document Placeholder Form](actions/create-document-placeholder-form.md) | `POST /organizations/{organization_id}/templates/{template_id}/document-placeholders` | [docs](https://docs.airslate.io/docs/airslate-api/document-placeholder-api) |
| [Create Organization](actions/create-organization.md) | `POST /organizations` | [docs](https://docs.airslate.io/docs/airslate-api/organizations-api/operations/create-a-organization) |
| [Create Organization Group](actions/create-organization-group.md) | `POST /organizations/{organization_id}/groups` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [Create Template](actions/create-template.md) | `POST /organizations/{organization_id}/templates` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api/operations/create-a-organization-template) |
| [Create Template Copy](actions/create-template-copy.md) | `POST /organizations/{organization_id}/templates/{template_id}/copy` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api/operations/create-a-organization-template-copy) |
| [Create Template Link](actions/create-template-link.md) | `PATCH /organizations/{organization_id}/templates/{template_id}/distribute` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Create Template Step](actions/create-template-step.md) | `POST /organizations/{organization_id}/templates/{template_id}/steps` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Create Template Step Jump](actions/create-template-step-jump.md) | `POST /organizations/{organization_id}/templates/{template_id}/step-jumps` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Create Template Version](actions/create-template-version.md) | `POST /organizations/{organization_id}/templates/{template_id}/versions` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Create Web Form](actions/create-web-form.md) | `POST /organizations/{organization_id}/templates/{template_id}/forms` | [docs](https://docs.airslate.io/docs/airslate-api/forms-api) |
| [Create Webhook](actions/create-webhook.md) | `POST /organizations/{organization_id}/webhooks` | [docs](https://docs.airslate.io/docs/airslate-api/webhooks-api) |
| [Create Workflow](actions/create-workflow.md) | `POST /organizations/{organization_id}/templates/{template_id}/flows` | [docs](https://docs.airslate.io/docs/airslate-api/flows-api) |
| [Create Workflow Batch](actions/create-workflow-batch.md) | `POST /organizations/{organization_id}/templates/{template_id}/flows/batch` | [docs](https://docs.airslate.io/docs/airslate-api/flows-api) |
| [Create Workflow Link](actions/create-workflow-link.md) | `POST /organizations/{organization_id}/templates/{template_id}/flows/{flow_id}/share` | [docs](https://docs.airslate.io/docs/airslate-api/flows-api) |
| [Delete Organization Group](actions/delete-organization-group.md) | `DELETE /organizations/{organization_id}/groups/{group_id}` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [Delete Template](actions/delete-template.md) | `DELETE /organizations/{organization_id}/templates/{template_id}` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api/operations/delete-a-organization-template) |
| [Delete Template Document](actions/delete-template-document.md) | `DELETE /organizations/{organization_id}/templates/{template_id}/documents/{document_id}` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api/operations/delete-a-organization-template-document) |
| [Delete Template Step](actions/delete-template-step.md) | `DELETE /organizations/{organization_id}/templates/{template_id}/steps/{step_id}` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Delete Template Step Jump](actions/delete-template-step-jump.md) | `DELETE /organizations/{organization_id}/templates/{template_id}/step-jumps/{jump_id}` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Delete Web Form Field](actions/delete-web-form-field.md) | `DELETE /organizations/{organization_id}/templates/{template_id}/forms/{form_id}/fields/{field_id}` | [docs](https://docs.airslate.io/docs/airslate-api/forms-api) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /organizations/{organization_id}/webhooks/{webhook_id}` | [docs](https://docs.airslate.io/docs/airslate-api/webhooks-api) |
| [Download Workflow Documents](actions/download-workflow-documents.md) | `GET /organizations/{organization_id}/templates/{template_id}/flows/{flow_id}/download` | [docs](https://docs.airslate.io/docs/airslate-api/flows-api) |
| [Generate Template DOCX Document](actions/generate-template-docx-document.md) | `POST /organizations/{organization_id}/templates/{template_id}/documents` | [docs](https://docs.airslate.io/docs/airslate-api/docgen-api/operations/create-a-organization-template-document) |
| [Get Log by ID](actions/get-log-by-id.md) | `GET /logs/{log_id}` | [docs](https://docs.airslate.io/docs/airslate-api/stats-api) |
| [Get Organization Settings](actions/get-organization-settings.md) | `GET /organizations/{organization_id}/settings` | [docs](https://docs.airslate.io/docs/airslate-api/organizations-api) |
| [Get Organization User by ID](actions/get-organization-user-by-id.md) | `GET /organizations/{organization_id}/users/{user_id}` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [Get Template by ID](actions/get-template-by-id.md) | `GET /organizations/{organization_id}/templates/{template_id}` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api/operations/get-a-organization-template) |
| [Get Template Document Assignments](actions/get-template-document-assignments.md) | `GET /organizations/{organization_id}/templates/{template_id}/documents/{document_id}/assignments` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Get Template Document by ID](actions/get-template-document-by-id.md) | `GET /organizations/{organization_id}/templates/{template_id}/documents/{document_id}` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api/operations/get-a-organization-template-document) |
| [Get Template Version Document Assignments](actions/get-template-version-document-assignments.md) | `GET /organizations/{organization_id}/templates/{template_id}/versions/{version_id}/documents/{document_id}/assignments` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Get Template Version Document by ID](actions/get-template-version-document-by-id.md) | `GET /organizations/{organization_id}/templates/{template_id}/versions/{version_id}/documents/{document_id}` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Get User Info](actions/get-user-info.md) | `GET https://oauth.airslate.com/public/userinfo` | [docs](https://docs.airslate.io/docs/airslate-api/authentication) |
| [Get Web Form Field by ID](actions/get-web-form-field-by-id.md) | `GET /organizations/{organization_id}/templates/{template_id}/forms/{form_id}/fields/{field_id}` | [docs](https://docs.airslate.io/docs/airslate-api/forms-api) |
| [Get Webhook by ID](actions/get-webhook-by-id.md) | `GET /organizations/{organization_id}/webhooks/{webhook_id}` | [docs](https://docs.airslate.io/docs/airslate-api/webhooks-api) |
| [Get Workflow by ID](actions/get-workflow-by-id.md) | `GET /organizations/{organization_id}/templates/{template_id}/flows/{flow_id}` | [docs](https://docs.airslate.io/docs/airslate-api/flows-api) |
| [Get Workflow Document by ID](actions/get-workflow-document-by-id.md) | `GET /organizations/{organization_id}/templates/{template_id}/flows/{flow_id}/documents/{document_id}` | [docs](https://docs.airslate.io/docs/airslate-api/flows-api) |
| [Get Workflow View Link](actions/get-workflow-view-link.md) | `GET /organizations/{organization_id}/templates/{template_id}/flows/{flow_id}/view` | [docs](https://docs.airslate.io/docs/airslate-api/flows-api) |
| [Invite Organization User](actions/invite-organization-user.md) | `POST /organizations/{organization_id}/users/invite` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [Invite Workflow Recipients](actions/invite-workflow-recipients.md) | `POST /organizations/{organization_id}/templates/{template_id}/flows/{flow_id}/invite` | [docs](https://docs.airslate.io/docs/airslate-api/flows-api) |
| [List Available Bots](actions/list-available-bots.md) | `GET /organizations/{organization_id}/bots` | [docs](https://docs.airslate.io/docs/airslate-api/bots-api) |
| [List Form Templates](actions/list-form-templates.md) | `GET /organizations/{organization_id}/forms/templates` | [docs](https://docs.airslate.io/docs/airslate-api/forms-api) |
| [List Group Members](actions/list-group-members.md) | `GET /organizations/{organization_id}/groups/{group_id}/members` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [List Logs](actions/list-logs.md) | `GET /logs` | [docs](https://docs.airslate.io/docs/airslate-api/stats-api) |
| [List Organization Groups](actions/list-organization-groups.md) | `GET /organizations/{organization_id}/groups` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [List Organization Users](actions/list-organization-users.md) | `GET /organizations/{organization_id}/users` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://docs.airslate.io/docs/airslate-api/organizations-api/operations/list-organizations) |
| [List Template Bots](actions/list-template-bots.md) | `GET /organizations/{organization_id}/templates/{template_id}/bots` | [docs](https://docs.airslate.io/docs/airslate-api/bots-api) |
| [List Template Documents](actions/list-template-documents.md) | `GET /organizations/{organization_id}/templates/{template_id}/documents` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api/operations/list-organization-template-documents) |
| [List Template Step Jumps](actions/list-template-step-jumps.md) | `GET /organizations/{organization_id}/templates/{template_id}/step-jumps` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [List Template Steps](actions/list-template-steps.md) | `GET /organizations/{organization_id}/templates/{template_id}/steps` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [List Template Tags](actions/list-template-tags.md) | `GET /organizations/{organization_id}/templates/{template_id}/tags` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [List Template Version Documents](actions/list-template-version-documents.md) | `GET /organizations/{organization_id}/templates/{template_id}/versions/{version_id}/documents` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api/operations/list-organization-template-version-documents) |
| [List Template Version Steps](actions/list-template-version-steps.md) | `GET /organizations/{organization_id}/templates/{template_id}/versions/{version_id}/steps` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [List Template Versions](actions/list-template-versions.md) | `GET /organizations/{organization_id}/templates/{template_id}/versions` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [List Template Workflows](actions/list-template-workflows.md) | `GET /organizations/{organization_id}/templates/{template_id}/flows` | [docs](https://docs.airslate.io/docs/airslate-api/flows-api) |
| [List Templates](actions/list-templates.md) | `GET /organizations/{organization_id}/templates` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api/operations/list-organization-templates) |
| [List Webhooks](actions/list-webhooks.md) | `GET /organizations/{organization_id}/webhooks` | [docs](https://docs.airslate.io/docs/airslate-api/webhooks-api) |
| [List Workflow Anonymous Links](actions/list-workflow-anonymous-links.md) | `GET /organizations/{organization_id}/templates/{template_id}/flows/{flow_id}/links` | [docs](https://docs.airslate.io/docs/airslate-api/flows-api) |
| [List Workflow Bot Logs](actions/list-workflow-bot-logs.md) | `GET /organizations/{organization_id}/templates/{template_id}/flows/{flow_id}/bot-logs` | [docs](https://docs.airslate.io/docs/airslate-api/flows-api) |
| [List Workflow Documents](actions/list-workflow-documents.md) | `GET /organizations/{organization_id}/templates/{template_id}/flows/{flow_id}/documents` | [docs](https://docs.airslate.io/docs/airslate-api/flows-api) |
| [Prefill Template Document](actions/prefill-template-document.md) | `PATCH /organizations/{organization_id}/templates/{template_id}/documents/{document_id}` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api/operations/modify-a-organization-template-document) |
| [Publish Template Version](actions/publish-template-version.md) | `PATCH /organizations/{organization_id}/templates/{template_id}/versions/{version_id}/publish` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Remove Group Member](actions/remove-group-member.md) | `DELETE /organizations/{organization_id}/groups/{group_id}/members/{user_id}` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [Remove Organization User](actions/remove-organization-user.md) | `DELETE /organizations/{organization_id}/users/{user_id}` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [Remove Template Bot](actions/remove-template-bot.md) | `DELETE /organizations/{organization_id}/templates/{template_id}/bots/{template_bot_id}` | [docs](https://docs.airslate.io/docs/airslate-api/bots-api) |
| [Remove Template Tag](actions/remove-template-tag.md) | `DELETE /organizations/{organization_id}/templates/{template_id}/tags/{tag_id}` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Rename Organization Group](actions/rename-organization-group.md) | `PATCH /organizations/{organization_id}/groups/{group_id}` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [Set Template Document Assignments](actions/set-template-document-assignments.md) | `POST /organizations/{organization_id}/templates/{template_id}/documents/{document_id}/assignments` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Update Document Placeholder Form](actions/update-document-placeholder-form.md) | `PATCH /organizations/{organization_id}/templates/{template_id}/document-placeholders/{form_id}` | [docs](https://docs.airslate.io/docs/airslate-api/document-placeholder-api) |
| [Update Group Member Role](actions/update-group-member-role.md) | `PATCH /organizations/{organization_id}/groups/{group_id}/members/{user_id}` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [Update Organization Settings](actions/update-organization-settings.md) | `PATCH /organizations/{organization_id}/settings` | [docs](https://docs.airslate.io/docs/airslate-api/organizations-api) |
| [Update Organization User](actions/update-organization-user.md) | `PATCH /organizations/{organization_id}/users/{user_id}` | [docs](https://docs.airslate.io/docs/airslate-api/team-management-api) |
| [Update Template](actions/update-template.md) | `PATCH /organizations/{organization_id}/templates/{template_id}` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api/operations/modify-a-organization-template) |
| [Update Template Bot](actions/update-template-bot.md) | `PATCH /organizations/{organization_id}/templates/{template_id}/bots/{template_bot_id}` | [docs](https://docs.airslate.io/docs/airslate-api/bots-api) |
| [Update Template Step](actions/update-template-step.md) | `PATCH /organizations/{organization_id}/templates/{template_id}/steps/{step_id}` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Update Template Step Jump](actions/update-template-step-jump.md) | `PATCH /organizations/{organization_id}/templates/{template_id}/step-jumps/{jump_id}` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api) |
| [Update Web Form](actions/update-web-form.md) | `PUT /organizations/{organization_id}/templates/{template_id}/forms/{form_id}` | [docs](https://docs.airslate.io/docs/airslate-api/forms-api) |
| [Update Web Form Field](actions/update-web-form-field.md) | `PUT /organizations/{organization_id}/templates/{template_id}/forms/{form_id}/fields/{field_id}` | [docs](https://docs.airslate.io/docs/airslate-api/forms-api) |
| [Upload Template Document](actions/upload-template-document.md) | `POST /organizations/{organization_id}/templates/{template_id}/documents` | [docs](https://docs.airslate.io/docs/airslate-api/templates-api/operations/create-a-organization-template-document) |
