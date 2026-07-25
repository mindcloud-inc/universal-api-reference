# <img src="https://images.mindcloud.co/apps/icons/kite-suite-icon_1776191617126.png" alt="Kite Suite logo" width="28" height="28"> Kite Suite: Universal API

Kite Suite is a work management and collaboration platform API for workspaces, projects, tasks, documents, forms, chats, dashboards, campaigns, and related workspace resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kiteSuiteCustom/latest
- **Category:** Productivity / Project Management
- **Actions:** 274
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.kitesuite.com
- **Vendor API docs:** https://api.kitesuite.com/swagger/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (274)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Create automation condition](actions/create-automation-condition.md) | POST |  |
| [Delete a single automation condition by ID](actions/delete-a-single-automation-condition-by-id.md) | DELETE |  |
| [Get a single automation condition by ID](actions/get-a-single-automation-condition-by-id.md) | GET |  |
| [Get all automation conditions](actions/get-all-automation-conditions.md) | GET |  |
| [Get all automation histories](actions/get-all-automation-histories.md) | GET |  |
| [Update a single automation condition by ID](actions/update-a-single-automation-condition-by-id.md) | PUT |  |

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Add Objects to Whiteboard](actions/add-objects-to-whiteboard.md) | POST |  |
| [Create new White Board](actions/create-new-white-board.md) | POST |  |
| [Delete WhiteBoard](actions/delete-white-board.md) | DELETE |  |
| [Get WhiteBoard by Id](actions/get-white-board-by-id.md) | GET |  |
| [Get WhiteBoard by project Id](actions/get-white-board-by-project-id.md) | GET |  |
| [Get Whiteboard Public URL](actions/get-whiteboard-public-url.md) | GET |  |
| [remove Whiteboard Objects](actions/remove-whiteboard-objects.md) | POST |  |
| [Undo Whiteboard Object Deletion](actions/undo-whiteboard-object-deletion.md) | PUT |  |
| [Update Multiple Whiteboard Objects](actions/update-multiple-whiteboard-objects.md) | PUT |  |
| [Update WhiteBoard](actions/update-white-board.md) | PUT |  |
| [Update Whiteboard Object](actions/update-whiteboard-object.md) | PUT |  |
| [Update Whiteboard Object Position](actions/update-whiteboard-object-position.md) | PUT |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Add or remove leads from a campaign](actions/add-or-remove-leads-from-a-campaign.md) | POST |  |
| [Create a new campaign](actions/create-a-new-campaign.md) | POST |  |
| [Create a new schedule](actions/create-a-new-schedule.md) | POST |  |
| [Create a new sequence](actions/create-a-new-sequence.md) | POST |  |
| [Delete a campaign by its ID](actions/delete-a-campaign-by-its-id.md) | DELETE |  |
| [Delete a schedule by ID](actions/delete-a-schedule-by-id.md) | DELETE |  |
| [Delete a sequence by ID](actions/delete-a-sequence-by-id.md) | DELETE |  |
| [Get all campaigns by workspace](actions/get-all-campaigns-by-workspace.md) | GET |  |
| [Get campaign analytics](actions/get-campaign-analytics.md) | GET |  |
| [Get campaign by ID](actions/get-campaign-by-id.md) | GET |  |
| [Get campaigns by account ID](actions/get-campaigns-by-account-id.md) | GET |  |
| [Update a campaign by its ID](actions/update-a-campaign-by-its-id.md) | PUT |  |
| [Update a schedule by ID](actions/update-a-schedule-by-id.md) | PUT |  |
| [Update a sequence by ID](actions/update-a-sequence-by-id.md) | PUT |  |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Api to create a conversation](actions/api-to-create-a-conversation.md) | POST |  |
| [Api to delete conversation from worksapce](actions/api-to-delete-conversation-from-worksapce.md) | DELETE |  |
| [Api to leave from conversation](actions/api-to-leave-from-conversation.md) | POST |  |
| [Api to update conversation](actions/api-to-update-conversation.md) | PUT |  |
| [Get conversations](actions/get-conversations.md) | GET |  |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST |  |
| [Create Custom Field (Drag Endpoint)](actions/create-custom-field-drag-endpoint.md) | POST |  |
| [Delete custom Field by Id](actions/delete-custom-field-by-id.md) | DELETE |  |
| [Get Predefined Field](actions/get-predefined-field.md) | GET |  |
| [Get Predefined Fields by project Id](actions/get-predefined-fields-by-project-id.md) | GET |  |
| [Reset default custom Field by project Id](actions/reset-default-custom-field-by-project-id.md) | PUT |  |
| [Update custom Field by Id](actions/update-custom-field-by-id.md) | PUT |  |
| [Update predefined Field](actions/update-predefined-field.md) | PUT |  |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [Create New Dashboard](actions/create-new-dashboard.md) | POST |  |
| [Delete dashboard By dashboard Id](actions/delete-dashboard-by-dashboard-id.md) | DELETE |  |
| [Delete Widget By Widget Id](actions/delete-widget-by-widget-id.md) | DELETE |  |
| [drag widget](actions/drag-widget.md) | PUT |  |
| [Get All Dashboard by User ID](actions/get-all-dashboard-by-user-id.md) | GET |  |
| [Get All Dashboard by Workspace ID](actions/get-all-dashboard-by-workspace-id.md) | GET |  |
| [Get Dashboard By Dashboard ID](actions/get-dashboard-by-dashboard-id.md) | GET |  |
| [Update Dashboard](actions/update-dashboard.md) | PUT |  |
| [update widget](actions/update-widget.md) | PUT |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Api to restore page history](actions/api-to-restore-page-history.md) | POST |  |
| [Api to update page history](actions/api-to-update-page-history.md) | PUT |  |
| [Create Document](actions/create-document.md) | POST |  |
| [Delete document](actions/delete-document.md) | DELETE |  |
| [Download document by document ID](actions/download-document-by-document-id.md) | GET |  |
| [Get all documents of workspace](actions/get-all-documents-of-workspace.md) | GET |  |
| [Get document by document ID](actions/get-document-by-document-id.md) | GET |  |
| [Get document by search](actions/get-document-by-search.md) | GET |  |
| [Get documents by project ID](actions/get-documents-by-project-id.md) | GET |  |
| [Get page history](actions/get-page-history.md) | GET |  |
| [Get Public Document by ID](actions/get-public-document-by-id.md) | GET |  |
| [Restore document](actions/restore-document.md) | PUT |  |
| [Update document](actions/update-document.md) | PUT |  |
| [Update multiple document](actions/update-multiple-document.md) | PUT |  |

### Epics

| Action | Method | Description |
| --- | --- | --- |
| [Create epic](actions/create-epic.md) | POST |  |
| [Delete Epic](actions/delete-epic.md) | DELETE |  |
| [Delete Epic comment](actions/delete-epic-comment.md) | DELETE |  |
| [Get All epic by projectID](actions/get-all-epic-by-project-id.md) | GET |  |
| [Get All epic by project key](actions/get-all-epic-by-project-key.md) | GET |  |
| [Reorder child issue](actions/reorder-child-issue.md) | PUT |  |
| [Update Epic](actions/update-epic.md) | PUT |  |
| [Upload Epic Attachment](actions/upload-epic-attachment.md) | POST |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete Attachment](actions/delete-attachment.md) | POST |  |
| [Get all conversations media](actions/get-all-conversations-media.md) | GET |  |
| [Upload Attachment](actions/upload-attachment.md) | POST |  |
| [Upload form Attachment](actions/upload-form-attachment.md) | POST |  |
| [Upload workspace Attachment](actions/upload-workspace-attachment.md) | POST |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Add Coupon](actions/add-coupon.md) | POST |  |
| [Create form](actions/create-form.md) | POST |  |
| [Create Form Condition](actions/create-form-condition.md) | POST |  |
| [Create Form Dropbox Action](actions/create-form-dropbox-action.md) | POST |  |
| [Create form Element](actions/create-form-element.md) | POST |  |
| [Create Form Google Calendar Event](actions/create-form-google-calendar-event.md) | POST |  |
| [Create Form Google Drive Action](actions/create-form-google-drive-action.md) | POST |  |
| [Create Form Google Sheets Integration](actions/create-form-google-sheets-integration.md) | POST |  |
| [Create Form Mailchimp Integration](actions/create-form-mailchimp-integration.md) | POST |  |
| [Create Form OneDrive Action](actions/create-form-one-drive-action.md) | POST |  |
| [Create Form Salesforce Action](actions/create-form-salesforce-action.md) | POST |  |
| [Create Form Theme](actions/create-form-theme.md) | POST |  |
| [Delete Coupon](actions/delete-coupon.md) | DELETE |  |
| [Delete form](actions/delete-form.md) | DELETE |  |
| [Delete Form Condition](actions/delete-form-condition.md) | DELETE |  |
| [Delete Form Dropbox Action](actions/delete-form-dropbox-action.md) | DELETE |  |
| [Delete form element](actions/delete-form-element.md) | DELETE |  |
| [Delete Form Google Calendar Event](actions/delete-form-google-calendar-event.md) | DELETE |  |
| [Delete Form Google Drive Action](actions/delete-form-google-drive-action.md) | DELETE |  |
| [Delete Form OneDrive Action](actions/delete-form-one-drive-action.md) | DELETE |  |
| [Delete Form Salesforce Action](actions/delete-form-salesforce-action.md) | DELETE |  |
| [Delete Form Theme](actions/delete-form-theme.md) | DELETE |  |
| [Drag form Element](actions/drag-form-element.md) | POST |  |
| [form submission](actions/form-submission.md) | POST |  |
| [Get form by form ID](actions/get-form-by-form-id.md) | GET |  |
| [Get form by public key](actions/get-form-by-public-key.md) | GET |  |
| [Get Form Element by ID](actions/get-form-element-by-id.md) | GET |  |
| [Get Form Integrations by Form ID](actions/get-form-integrations-by-form-id.md) | GET |  |
| [Get Form Theme Templates](actions/get-form-theme-templates.md) | GET |  |
| [Get forms by project ID](actions/get-forms-by-project-id.md) | GET |  |
| [Get Invoice Preview](actions/get-invoice-preview.md) | GET |  |
| [Get workspace forms](actions/get-workspace-forms.md) | GET |  |
| [Redeem Coupon](actions/redeem-coupon.md) | POST |  |
| [Remove Form Integration](actions/remove-form-integration.md) | DELETE |  |
| [Update Coupon](actions/update-coupon.md) | PUT |  |
| [Update form](actions/update-form.md) | PUT |  |
| [Update Form Condition](actions/update-form-condition.md) | PUT |  |
| [Update Form Design](actions/update-form-design.md) | PUT |  |
| [Update Form Dropbox Action](actions/update-form-dropbox-action.md) | PUT |  |
| [Update form Element](actions/update-form-element.md) | PUT |  |
| [Update Form Google Calendar Event](actions/update-form-google-calendar-event.md) | PUT |  |
| [Update Form Google Drive Action](actions/update-form-google-drive-action.md) | PUT |  |
| [Update Form Google Sheets Integration](actions/update-form-google-sheets-integration.md) | PUT |  |
| [Update Form Mailchimp Integration](actions/update-form-mailchimp-integration.md) | PUT |  |
| [Update Form OneDrive Action](actions/update-form-one-drive-action.md) | PUT |  |
| [Update Form payment](actions/update-form-payment.md) | PUT |  |
| [Update Form Salesforce Action](actions/update-form-salesforce-action.md) | PUT |  |
| [update form submission](actions/update-form-submission.md) | PUT |  |
| [Update Form Thank You Page](actions/update-form-thank-you-page.md) | PUT |  |
| [Update Product Position in Form Element](actions/update-product-position-in-form-element.md) | PUT |  |
| [update submission](actions/update-submission.md) | PUT |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [API to create a new Gantt entry](actions/a-pi-to-create-a-new-gantt-entry.md) | POST |  |
| [API to update an existing Gantt entry](actions/a-pi-to-update-an-existing-gantt-entry.md) | PUT |  |
| [Api to create a custom color](actions/api-to-create-a-custom-color.md) | POST |  |
| [Api to update custom color](actions/api-to-update-custom-color.md) | PUT |  |
| [Create Check task](actions/create-check-task.md) | POST |  |
| [Create workspace backup](actions/create-workspace-backup.md) | POST |  |
| [Delete Field by Id](actions/delete-field-by-id.md) | DELETE |  |
| [Export All imports by projectID](actions/export-all-imports-by-project-id.md) | GET |  |
| [Export All task by projectID](actions/export-all-task-by-project-id.md) | GET |  |
| [Get Gantt chart by project ID](actions/get-gantt-chart-by-project-id.md) | GET |  |
| [get workspace backup](actions/get-workspace-backup.md) | GET |  |
| [Import from Clickup](actions/import-from-clickup.md) | POST |  |
| [Import from CSV](actions/import-from-csv.md) | POST |  |
| [Import from CSV (Import Endpoint)](actions/import-from-csv-import-endpoint.md) | POST |  |
| [Import From Jira](actions/import-from-jira.md) | POST |  |
| [Update Field by Id](actions/update-field-by-id.md) | PUT |  |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Create label from project.](actions/create-label-from-project.md) | POST |  |
| [delete label from project.](actions/delete-label-from-project.md) | DELETE |  |
| [Update label from project.](actions/update-label-from-project.md) | PUT |  |
| [update meeting .](actions/update-meeting.md) | PUT |  |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create new list in project](actions/create-new-list-in-project.md) | POST |  |
| [Delete List By ID](actions/delete-list-by-id.md) | DELETE |  |
| [Get List By Project ID](actions/get-list-by-project-id.md) | GET |  |
| [move List position](actions/move-list-position.md) | POST |  |
| [Update task List from one to another](actions/update-task-list-from-one-to-another.md) | PUT |  |
| [Update the ListName](actions/update-the-list-name.md) | PUT |  |

### Meetings

| Action | Method | Description |
| --- | --- | --- |
| [Create meeting in workspace.](actions/create-meeting-in-workspace.md) | POST |  |
| [delete meeting .](actions/delete-meeting.md) | DELETE |  |
| [Get Meeting.](actions/get-meeting.md) | GET |  |
| [Get user's meeting in current workspace.](actions/get-users-meeting-in-current-workspace.md) | GET |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Api to delete message from group](actions/api-to-delete-message-from-group.md) | DELETE |  |
| [Api to send message to Project Group](actions/api-to-send-message-to-project-group.md) | POST |  |
| [Api to update message from conversation](actions/api-to-update-message-from-conversation.md) | PUT |  |
| [Create a new communication draft](actions/create-a-new-communication-draft.md) | POST |  |
| [Delete multiple communications.](actions/delete-multiple-communications.md) | POST |  |
| [Get communication](actions/get-communication.md) | GET |  |
| [Get communications of a specific thread.](actions/get-communications-of-a-specific-thread.md) | GET |  |
| [Get messages based on pagination](actions/get-messages-based-on-pagination.md) | GET |  |
| [Send Email through app](actions/send-email-through-app.md) | POST |  |
| [Track email link clicks and redirect to the target link.](actions/track-email-link-clicks-and-redirect-to-the-target-link.md) | GET |  |
| [Track email open status through a tracking pixel.](actions/track-email-open-status-through-a-tracking-pixel.md) | GET |  |
| [Unsubscribe from communication emails.](actions/unsubscribe-from-communication-emails.md) | GET |  |
| [Update communication](actions/update-communication.md) | PUT |  |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Get notification by user Id](actions/get-notification-by-user-id.md) | GET |  |
| [Update notification of user](actions/update-notification-of-user.md) | PUT |  |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST |  |
| [Delete page](actions/delete-page.md) | DELETE |  |
| [Drag page](actions/drag-page.md) | POST |  |
| [Duplicate Page](actions/duplicate-page.md) | POST |  |
| [Get page by page ID](actions/get-page-by-page-id.md) | GET |  |
| [Move page to another document](actions/move-page-to-another-document.md) | POST |  |
| [Update page](actions/update-page.md) | PUT |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Add Members to project.](actions/add-members-to-project.md) | POST |  |
| [Check project key to workspace.](actions/check-project-key-to-workspace.md) | GET |  |
| [Create new project](actions/create-new-project.md) | POST |  |
| [Delete project by id](actions/delete-project-by-id.md) | DELETE |  |
| [Get all project data by project Id](actions/get-all-project-data-by-project-id.md) | GET |  |
| [Get project by Id](actions/get-project-by-id.md) | GET |  |
| [Get project list fields.](actions/get-project-list-fields.md) | GET |  |
| [Get projects by owner Id](actions/get-projects-by-owner-id.md) | GET |  |
| [Get projects by ProjectLeader Id](actions/get-projects-by-project-leader-id.md) | GET |  |
| [Get projects,lists,epics by workspace Id](actions/get-projectslistsepics-by-workspace-id.md) | GET |  |
| [Get projects,lists,sprints,epics by workspace Id](actions/get-projectslistssprintsepics-by-workspace-id.md) | GET |  |
| [Get trashed project lists.](actions/get-trashed-project-lists.md) | GET |  |
| [Remove member from project.](actions/remove-member-from-project.md) | DELETE |  |
| [Restore project](actions/restore-project.md) | POST |  |
| [Update member's role to project.](actions/update-members-role-to-project.md) | PUT |  |
| [Update Multiple Members to project.](actions/update-multiple-members-to-project.md) | PUT |  |
| [Update Project](actions/update-project.md) | PUT |  |
| [Update project list fields.](actions/update-project-list-fields.md) | PUT |  |

### Releases

| Action | Method | Description |
| --- | --- | --- |
| [Create new release](actions/create-new-release.md) | POST |  |
| [Delete Release](actions/delete-release.md) | DELETE |  |
| [Get Release by Id](actions/get-release-by-id.md) | GET |  |
| [Get Release by project Id](actions/get-release-by-project-id.md) | GET |  |
| [Update Release](actions/update-release.md) | PUT |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get all Sprint activity data by project Id](actions/get-all-sprint-activity-data-by-project-id.md) | GET |  |
| [Get specified report data by projectId](actions/get-specified-report-data-by-project-id.md) | GET |  |
| [sync data by project Id](actions/sync-data-by-project-id.md) | POST |  |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Add New Project Roles](actions/add-new-project-roles.md) | POST |  |
| [Add new role in workspace](actions/add-new-role-in-workspace.md) | POST |  |
| [Delete Project Role By Role Id](actions/delete-project-role-by-role-id.md) | DELETE |  |
| [Delete workspace roles by role ID](actions/delete-workspace-roles-by-role-id.md) | DELETE |  |
| [Get All Default Project Roles](actions/get-all-default-project-roles.md) | GET |  |
| [Get all workspace roles](actions/get-all-workspace-roles.md) | GET |  |
| [Get Project Roles By Project ID](actions/get-project-roles-by-project-id.md) | GET |  |
| [Get Project Roles By User ID](actions/get-project-roles-by-user-id.md) | GET |  |
| [Get workspace roles by tenant ID](actions/get-workspace-roles-by-tenant-id.md) | GET |  |
| [Update Role](actions/update-role.md) | PUT |  |
| [Update workspace roles by role ID](actions/update-workspace-roles-by-role-id.md) | PUT |  |

### Sprints

| Action | Method | Description |
| --- | --- | --- |
| [Add New Sprint](actions/add-new-sprint.md) | POST |  |
| [Complete Sprint By Sprint Id](actions/complete-sprint-by-sprint-id.md) | POST |  |
| [Delete Sprint By Sprint Id](actions/delete-sprint-by-sprint-id.md) | DELETE |  |
| [Get completed sprints by projectID.](actions/get-completed-sprints-by-project-id.md) | GET |  |
| [Get sprint by ID.](actions/get-sprint-by-id.md) | GET |  |
| [Get sprints by project ID](actions/get-sprints-by-project-id.md) | GET |  |
| [Update Sprint](actions/update-sprint.md) | PUT |  |
| [Update Tasks in sprint](actions/update-tasks-in-sprint.md) | PUT |  |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan](actions/get-plan.md) | GET |  |
| [Get Plan By ID](actions/get-plan-by-id.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [change parent of a task by task Id](actions/change-parent-of-a-task-by-task-id.md) | PUT |  |
| [clone task](actions/clone-task.md) | POST |  |
| [Create sub task](actions/create-sub-task.md) | POST |  |
| [Create task](actions/create-task.md) | POST |  |
| [Delete comments](actions/delete-comments.md) | DELETE |  |
| [Delete spents](actions/delete-spents.md) | DELETE |  |
| [Delete task](actions/delete-task.md) | DELETE |  |
| [Get All sub task by project ID](actions/get-all-sub-task-by-project-id.md) | GET |  |
| [Get All task by project ID](actions/get-all-task-by-project-id.md) | GET |  |
| [Get task by assignee ID](actions/get-task-by-assignee-id.md) | GET |  |
| [Get task by serial number.](actions/get-task-by-serial-number.md) | GET |  |
| [Get task by task ID](actions/get-task-by-task-id.md) | GET |  |
| [Get trash task by ID](actions/get-trash-task-by-id.md) | GET |  |
| [move task](actions/move-task.md) | POST |  |
| [Reorder sub task by sub task Id](actions/reorder-sub-task-by-sub-task-id.md) | PUT |  |
| [update multiple tasks](actions/update-multiple-tasks.md) | PUT |  |
| [Update task by Id](actions/update-task-by-id.md) | PUT |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET |  |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Create new Team](actions/create-new-team.md) | POST |  |
| [Delete Team](actions/delete-team.md) | DELETE |  |
| [Get Team by Id](actions/get-team-by-id.md) | GET |  |
| [Update Team](actions/update-team.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User By Id](actions/get-user-by-id-get-api-v1-user-id.md) | GET |  |
| [Get User By workspace ID](actions/get-user-by-workspace-idget-api-v1-user-workspace-id.md) | GET |  |
| [Update User Avatar By ID](actions/update-user-avatar-by-idpatch-api-v1-user-avatar-id.md) | PUT |  |
| [Update User By ID](actions/update-user-by-idpatch-api-v1-user-id.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create directory](actions/create-directory.md) | POST |  |
| [Delete Directory](actions/delete-directory.md) | DELETE |  |
| [Get all Directories of workspace](actions/get-all-directories-of-workspace.md) | GET |  |
| [Get Directory by Id](actions/get-directory-by-id.md) | GET |  |
| [Sync directory](actions/sync-directory.md) | POST |  |
| [Update Directory](actions/update-directory.md) | PUT |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Add members in workspace.](actions/add-members-in-workspace.md) | POST |  |
| [Check Workspace Key Existence](actions/check-workspace-key-existence.md) | POST |  |
| [Create workspace](actions/create-workspace.md) | POST |  |
| [Get workspaces by user ID](actions/get-workspaces-by-user-id.md) | GET |  |
| [Remove member in workspace.](actions/remove-member-in-workspace.md) | DELETE |  |
| [Search All Data in Workspace](actions/search-all-data-in-workspace.md) | GET |  |
| [Update multiple members in workspace.](actions/update-multiple-members-in-workspace.md) | PUT |  |
| [Update role in workspace by workspace Id.](actions/update-role-in-workspace-by-workspace-id.md) | PUT |  |
| [Update workspace](actions/update-workspace.md) | PUT |  |
| [Update Workspace Avatar](actions/update-workspace-avatar.md) | PUT |  |

