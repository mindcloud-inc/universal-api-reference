# <img src="https://images.mindcloud.co/apps/icons/airslate_1776179277947.png" alt="Airslate logo" width="28" height="28"> Airslate: Universal API

Airslate is a document workflow automation platform for organizations to create, send, manage, and track document-driven workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/airslate/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 84
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.airslate.com
- **Vendor API docs:** https://docs.airslate.io/docs/airslate-api/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airslate/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (84)

### Bot Logs

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Bot Logs](actions/list-workflow-bot-logs.md) | GET | Retrieves workflow bot logs from airSlate. |

### Bots

| Action | Method | Description |
| --- | --- | --- |
| [Attach Template Bot](actions/attach-template-bot.md) | POST | Attaches a bot to a template in airSlate. |
| [List Available Bots](actions/list-available-bots.md) | GET | Retrieves available bot records from airSlate. |
| [List Template Bots](actions/list-template-bots.md) | GET | Retrieves template bot records from airSlate. |
| [Remove Template Bot](actions/remove-template-bot.md) | DELETE | Removes a template bot from airSlate. |
| [Update Template Bot](actions/update-template-bot.md) | PUT | Updates a template bot in airSlate. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Add Web Form Field](actions/add-web-form-field.md) | POST | Adds a field to a web form in airSlate. |
| [Delete Web Form Field](actions/delete-web-form-field.md) | DELETE | Deletes a web form field from airSlate. |
| [Get Web Form Field by ID](actions/get-web-form-field-by-id.md) | GET | Retrieves a web form field by ID from airSlate. |
| [Update Web Form Field](actions/update-web-form-field.md) | PUT | Updates a web form field in airSlate. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Delete Template Document](actions/delete-template-document.md) | DELETE | Deletes a template document from airSlate. |
| [Download Workflow Documents](actions/download-workflow-documents.md) | GET | Downloads workflow document files from airSlate. |
| [Generate Template DOCX Document](actions/generate-template-docx-document.md) | POST | Creates a DOCX template document in airSlate. |
| [Get Template Document by ID](actions/get-template-document-by-id.md) | GET | Retrieves a template document by ID from airSlate. |
| [Get Template Version Document by ID](actions/get-template-version-document-by-id.md) | GET | Retrieves a template version document by ID from airSlate. |
| [Get Workflow Document by ID](actions/get-workflow-document-by-id.md) | GET | Retrieves a workflow document by ID from airSlate. |
| [List Template Documents](actions/list-template-documents.md) | GET | Retrieves template document records from airSlate. |
| [List Template Version Documents](actions/list-template-version-documents.md) | GET | Retrieves template version documents from airSlate. |
| [List Workflow Documents](actions/list-workflow-documents.md) | GET | Retrieves workflow document records from airSlate. |
| [Prefill Template Document](actions/prefill-template-document.md) | PUT | Prefills a template document in airSlate. |
| [Upload Template Document](actions/upload-template-document.md) | POST | Uploads a template document to airSlate. |

### Field Assignments

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Document Assignments](actions/get-template-document-assignments.md) | GET | Retrieves template document assignments from airSlate. |
| [Get Template Version Document Assignments](actions/get-template-version-document-assignments.md) | GET | Retrieves template version document assignments from airSlate. |
| [Set Template Document Assignments](actions/set-template-document-assignments.md) | POST | Sets template document assignments in airSlate. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Placeholder Form](actions/create-document-placeholder-form.md) | POST | Creates a document placeholder form in airSlate. |
| [Create Web Form](actions/create-web-form.md) | POST | Creates a web form in airSlate. |
| [List Form Templates](actions/list-form-templates.md) | GET | Retrieves form template records from airSlate. |
| [Update Document Placeholder Form](actions/update-document-placeholder-form.md) | PUT | Updates a document placeholder form in airSlate. |
| [Update Web Form](actions/update-web-form.md) | PUT | Updates a web form in airSlate. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization Group](actions/create-organization-group.md) | POST | Creates a new organization group in airSlate. |
| [Delete Organization Group](actions/delete-organization-group.md) | DELETE | Deletes an organization group from airSlate. |
| [List Organization Groups](actions/list-organization-groups.md) | GET | Retrieves organization group records from airSlate. |
| [Rename Organization Group](actions/rename-organization-group.md) | PUT | Renames an organization group in airSlate. |

### Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Log by ID](actions/get-log-by-id.md) | GET | Retrieves a log by ID from airSlate. |
| [List Logs](actions/list-logs.md) | GET | Retrieves all log records from airSlate. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Add Group Members](actions/add-group-members.md) | POST | Adds members to a group in airSlate. |
| [List Group Members](actions/list-group-members.md) | GET | Retrieves group member records from airSlate. |
| [Remove Group Member](actions/remove-group-member.md) | DELETE | Removes a group member from airSlate. |
| [Update Group Member Role](actions/update-group-member-role.md) | PUT | Updates a group member role in airSlate. |

### Organization Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Settings](actions/get-organization-settings.md) | GET | Retrieves organization settings details from airSlate. |
| [Update Organization Settings](actions/update-organization-settings.md) | PUT | Updates existing organization settings in airSlate. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates a new organization in airSlate. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves all organization records from airSlate. |

### Step Jumps

| Action | Method | Description |
| --- | --- | --- |
| [Create Template Step Jump](actions/create-template-step-jump.md) | POST | Creates a template step jump in airSlate. |
| [Delete Template Step Jump](actions/delete-template-step-jump.md) | DELETE | Deletes a template step jump from airSlate. |
| [List Template Step Jumps](actions/list-template-step-jumps.md) | GET | Retrieves template step jumps from airSlate. |
| [Update Template Step Jump](actions/update-template-step-jump.md) | PUT | Updates a template step jump in airSlate. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Add Template Tag](actions/add-template-tag.md) | POST | Adds a tag to a template in airSlate. |
| [List Template Tags](actions/list-template-tags.md) | GET | Retrieves template tag records from airSlate. |
| [Remove Template Tag](actions/remove-template-tag.md) | DELETE | Removes a tag from a template in airSlate. |

### Template Links

| Action | Method | Description |
| --- | --- | --- |
| [Create Template Link](actions/create-template-link.md) | POST | Creates a template link in airSlate. |

### Template Steps

| Action | Method | Description |
| --- | --- | --- |
| [Create Template Step](actions/create-template-step.md) | POST | Creates a new template step in airSlate. |
| [Delete Template Step](actions/delete-template-step.md) | DELETE | Deletes a template step from airSlate. |
| [List Template Steps](actions/list-template-steps.md) | GET | Retrieves template step records from airSlate. |
| [List Template Version Steps](actions/list-template-version-steps.md) | GET | Retrieves template version steps from airSlate. |
| [Update Template Step](actions/update-template-step.md) | PUT | Updates a template step in airSlate. |

### Template Versions

| Action | Method | Description |
| --- | --- | --- |
| [Create Template Version](actions/create-template-version.md) | POST | Creates a new template version in airSlate. |
| [List Template Versions](actions/list-template-versions.md) | GET | Retrieves template version records from airSlate. |
| [Publish Template Version](actions/publish-template-version.md) | PUT | Publishes a template version in airSlate. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in airSlate. |
| [Create Template Copy](actions/create-template-copy.md) | POST | Creates a copy of a template in airSlate. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from airSlate. |
| [Get Template by ID](actions/get-template-by-id.md) | GET | Retrieves a template by ID from airSlate. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from an airSlate organization. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in airSlate. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Organization User Invite](actions/cancel-organization-user-invite.md) | DELETE | Cancels an organization user invite in airSlate. |
| [Get Organization User by ID](actions/get-organization-user-by-id.md) | GET | Retrieves an organization user by ID from airSlate. |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves user profile details from airSlate. |
| [Invite Organization User](actions/invite-organization-user.md) | POST | Invites a user to an organization in airSlate. |
| [List Organization Users](actions/list-organization-users.md) | GET | Retrieves organization user records from airSlate. |
| [Remove Organization User](actions/remove-organization-user.md) | DELETE | Removes an organization user from airSlate. |
| [Update Organization User](actions/update-organization-user.md) | PUT | Updates an organization user in airSlate. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in airSlate. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from airSlate. |
| [Get Webhook by ID](actions/get-webhook-by-id.md) | GET | Retrieves a webhook by ID from airSlate. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves all webhook records from airSlate. |

### Workflow Links

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow Link](actions/create-workflow-link.md) | POST | Creates a workflow link in airSlate. |
| [Get Workflow View Link](actions/get-workflow-view-link.md) | GET | Retrieves a workflow view link from airSlate. |
| [List Workflow Anonymous Links](actions/list-workflow-anonymous-links.md) | GET | Retrieves anonymous workflow links from airSlate. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a new workflow in airSlate. |
| [Create Workflow Batch](actions/create-workflow-batch.md) | POST | Creates a workflow batch in airSlate. |
| [Get Workflow by ID](actions/get-workflow-by-id.md) | GET | Retrieves a workflow by ID from airSlate. |
| [Invite Workflow Recipients](actions/invite-workflow-recipients.md) | POST | Invites recipients to a workflow in airSlate. |
| [List Template Workflows](actions/list-template-workflows.md) | GET | Retrieves workflows for a template in airSlate. |

