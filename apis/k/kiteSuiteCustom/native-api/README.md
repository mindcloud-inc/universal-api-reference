# Kite Suite: Native API Reference

A consolidated summary of Kite Suite's API configuration and 272 documented operations, with links to official documentation.

- **Official docs:** https://api.kitesuite.com/swagger/
- **API base URL:** `https://api.kitesuite.com`

## Authentication

### Workspace API Token

Custom auth for Kite Suite using the exact headers api-token and workspace.

### Credentials

- **API Token:** `apiToken` · required · Kite Suite API token used for the shared `api-token` header.
- **Workspace Key:** `workspace` · required · Workspace key used for the shared `workspace` header.

Send these headers with each API request:

```http
api-token: <apiToken>
workspace: <workspace>
```

[Official authentication documentation](https://api.kitesuite.com/swagger/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (272 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [API to create a new Gantt entry](actions/a-pi-to-create-a-new-gantt-entry.md) | `POST /api/v1/gantt` | [docs](https://api.kitesuite.com/swagger/) |
| [API to update an existing Gantt entry](actions/a-pi-to-update-an-existing-gantt-entry.md) | `PATCH /api/v1/gantt/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Add Coupon](actions/add-coupon.md) | `POST /api/v1/form/coupon` | [docs](https://api.kitesuite.com/swagger/) |
| [Add members in workspace.](actions/add-members-in-workspace.md) | `POST /api/v1/workspace/member` | [docs](https://api.kitesuite.com/swagger/) |
| [Add Members to project.](actions/add-members-to-project.md) | `POST /api/v1/project/member` | [docs](https://api.kitesuite.com/swagger/) |
| [Add New Project Roles](actions/add-new-project-roles.md) | `POST /api/v1/project-role` | [docs](https://api.kitesuite.com/swagger/) |
| [Add new role in workspace](actions/add-new-role-in-workspace.md) | `POST /api/v1/workspace-role` | [docs](https://api.kitesuite.com/swagger/) |
| [Add New Sprint](actions/add-new-sprint.md) | `POST /api/v1/sprint` | [docs](https://api.kitesuite.com/swagger/) |
| [Add Objects to Whiteboard](actions/add-objects-to-whiteboard.md) | `POST /api/v1/white-board/object` | [docs](https://api.kitesuite.com/swagger/) |
| [Add or remove leads from a campaign](actions/add-or-remove-leads-from-a-campaign.md) | `POST /api/v1/campaign/lead` | [docs](https://api.kitesuite.com/swagger/) |
| [Api to create a conversation](actions/api-to-create-a-conversation.md) | `POST /api/v1/conversation` | [docs](https://api.kitesuite.com/swagger/) |
| [Api to create a custom color](actions/api-to-create-a-custom-color.md) | `POST /api/v1/custom-color` | [docs](https://api.kitesuite.com/swagger/) |
| [Api to delete conversation from worksapce](actions/api-to-delete-conversation-from-worksapce.md) | `DELETE /api/v1/conversation/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Api to delete message from group](actions/api-to-delete-message-from-group.md) | `DELETE /api/v1/chat/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Api to leave from conversation](actions/api-to-leave-from-conversation.md) | `POST /api/v1/conversation/leave` | [docs](https://api.kitesuite.com/swagger/) |
| [Api to restore page history](actions/api-to-restore-page-history.md) | `POST /api/v1/history/restore` | [docs](https://api.kitesuite.com/swagger/) |
| [Api to send message to Project Group](actions/api-to-send-message-to-project-group.md) | `POST /api/v1/chat` | [docs](https://api.kitesuite.com/swagger/) |
| [Api to update conversation](actions/api-to-update-conversation.md) | `PATCH /api/v1/conversation/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Api to update custom color](actions/api-to-update-custom-color.md) | `PATCH /api/v1/custom-color/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Api to update message from conversation](actions/api-to-update-message-from-conversation.md) | `PATCH /api/v1/chat/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Api to update page history](actions/api-to-update-page-history.md) | `PATCH /api/v1/history/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [change parent of a task by task Id](actions/change-parent-of-a-task-by-task-id.md) | `POST /api/v1/task/convert` | [docs](https://api.kitesuite.com/swagger/) |
| [Check project key to workspace.](actions/check-project-key-to-workspace.md) | `GET /api/v1/project/key/exist` | [docs](https://api.kitesuite.com/swagger/) |
| [Check Workspace Key Existence](actions/check-workspace-key-existence.md) | `POST /api/v1/workspace/key-exists` | [docs](https://api.kitesuite.com/swagger/) |
| [clone task](actions/clone-task.md) | `POST /api/v1/task/clone` | [docs](https://api.kitesuite.com/swagger/) |
| [Complete Sprint By Sprint Id](actions/complete-sprint-by-sprint-id.md) | `POST /api/v1/sprint/complete` | [docs](https://api.kitesuite.com/swagger/) |
| [Create a new campaign](actions/create-a-new-campaign.md) | `POST /api/v1/campaign` | [docs](https://api.kitesuite.com/swagger/) |
| [Create a new communication draft](actions/create-a-new-communication-draft.md) | `POST /api/v1/communication` | [docs](https://api.kitesuite.com/swagger/) |
| [Create a new schedule](actions/create-a-new-schedule.md) | `POST /api/v1/campaign/schedule` | [docs](https://api.kitesuite.com/swagger/) |
| [Create a new sequence](actions/create-a-new-sequence.md) | `POST /api/v1/campaign/sequence` | [docs](https://api.kitesuite.com/swagger/) |
| [Create automation condition](actions/create-automation-condition.md) | `POST /api/v1/automation` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Check task](actions/create-check-task.md) | `POST /api/v1/check-list/` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /api/v1/custom-field/` | [docs](https://api.kitesuite.com/swagger/) |
| [Create directory](actions/create-directory.md) | `POST /api/v1/directory` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Document](actions/create-document.md) | `POST /api/v1/document` | [docs](https://api.kitesuite.com/swagger/) |
| [Create epic](actions/create-epic.md) | `POST /api/v1/epic` | [docs](https://api.kitesuite.com/swagger/) |
| [Create form](actions/create-form.md) | `POST /api/v1/form` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Form Condition](actions/create-form-condition.md) | `POST /api/v1/form/condition` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Form Dropbox Action](actions/create-form-dropbox-action.md) | `POST /api/v1/form/integration/dropbox/actions` | [docs](https://api.kitesuite.com/swagger/) |
| [Create form Element](actions/create-form-element.md) | `POST /api/v1/form/element` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Form Google Calendar Event](actions/create-form-google-calendar-event.md) | `POST /api/v1/form/integration/google-calendar/events` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Form Google Drive Action](actions/create-form-google-drive-action.md) | `POST /api/v1/form/integration/google-drive/actions` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Form Google Sheets Integration](actions/create-form-google-sheets-integration.md) | `POST /api/v1/form/integration/google-sheet` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Form Mailchimp Integration](actions/create-form-mailchimp-integration.md) | `POST /api/v1/form/integration/mailchimp` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Form OneDrive Action](actions/create-form-one-drive-action.md) | `POST /api/v1/form/integration/one-drive/actions` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Form Salesforce Action](actions/create-form-salesforce-action.md) | `POST /api/v1/form/integration/salesforce/actions` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Form Theme](actions/create-form-theme.md) | `POST /api/v1/form/theme` | [docs](https://api.kitesuite.com/swagger/) |
| [Create label from project.](actions/create-label-from-project.md) | `POST /api/v1/label` | [docs](https://api.kitesuite.com/swagger/) |
| [Create meeting in workspace.](actions/create-meeting-in-workspace.md) | `POST /api/v1/meeting` | [docs](https://api.kitesuite.com/swagger/) |
| [Create New Dashboard](actions/create-new-dashboard.md) | `POST /api/v1/dashboard` | [docs](https://api.kitesuite.com/swagger/) |
| [Create new list in project](actions/create-new-list-in-project.md) | `POST /api/v1/list` | [docs](https://api.kitesuite.com/swagger/) |
| [Create new project](actions/create-new-project.md) | `POST /api/v1/project` | [docs](https://api.kitesuite.com/swagger/) |
| [Create new release](actions/create-new-release.md) | `POST /api/v1/release` | [docs](https://api.kitesuite.com/swagger/) |
| [Create new Team](actions/create-new-team.md) | `POST /api/v1/team` | [docs](https://api.kitesuite.com/swagger/) |
| [Create new White Board](actions/create-new-white-board.md) | `POST /api/v1/white-board` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Page](actions/create-page.md) | `POST /api/v1/page` | [docs](https://api.kitesuite.com/swagger/) |
| [Create sub task](actions/create-sub-task.md) | `POST /api/v1/task/sub-task` | [docs](https://api.kitesuite.com/swagger/) |
| [Create task](actions/create-task.md) | `POST /api/v1/task` | [docs](https://api.kitesuite.com/swagger/) |
| [Create workspace](actions/create-workspace.md) | `POST /api/v1/workspace` | [docs](https://api.kitesuite.com/swagger/) |
| [Create workspace backup](actions/create-workspace-backup.md) | `POST /api/v1/import-export/backup` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete a campaign by its ID](actions/delete-a-campaign-by-its-id.md) | `DELETE /api/v1/campaign/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete a schedule by ID](actions/delete-a-schedule-by-id.md) | `DELETE /api/v1/campaign/schedule/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete a sequence by ID](actions/delete-a-sequence-by-id.md) | `DELETE /api/v1/campaign/sequence/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete a single automation condition by ID](actions/delete-a-single-automation-condition-by-id.md) | `DELETE /api/v1/automation/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Attachment](actions/delete-attachment.md) | `POST /api/v1/media/attachment` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete comments](actions/delete-comments.md) | `DELETE /api/v1/task/comments/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Coupon](actions/delete-coupon.md) | `DELETE /api/v1/form/coupon/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete custom Field by Id](actions/delete-custom-field-by-id.md) | `DELETE /api/v1/custom-field/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete dashboard By dashboard Id](actions/delete-dashboard-by-dashboard-id.md) | `DELETE /api/v1/dashboard/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Directory](actions/delete-directory.md) | `DELETE /api/v1/directory/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete document](actions/delete-document.md) | `DELETE /api/v1/document/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Epic](actions/delete-epic.md) | `DELETE /api/v1/epic/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Epic comment](actions/delete-epic-comment.md) | `DELETE /api/v1/epic/comment/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Field by Id](actions/delete-field-by-id.md) | `DELETE /api/v1/check-list/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete form](actions/delete-form.md) | `DELETE /api/v1/form/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Form Condition](actions/delete-form-condition.md) | `DELETE /api/v1/form/condition/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Form Dropbox Action](actions/delete-form-dropbox-action.md) | `DELETE /api/v1/form/integration/dropbox/actions/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete form element](actions/delete-form-element.md) | `DELETE /api/v1/form/element/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Form Google Calendar Event](actions/delete-form-google-calendar-event.md) | `DELETE /api/v1/form/integration/google-calendar/events/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Form Google Drive Action](actions/delete-form-google-drive-action.md) | `DELETE /api/v1/form/integration/google-drive/actions/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Form OneDrive Action](actions/delete-form-one-drive-action.md) | `DELETE /api/v1/form/integration/one-drive/actions/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Form Salesforce Action](actions/delete-form-salesforce-action.md) | `DELETE /api/v1/form/integration/salesforce/actions/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Form Theme](actions/delete-form-theme.md) | `DELETE /api/v1/form/theme/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [delete label from project.](actions/delete-label-from-project.md) | `DELETE /api/v1/label/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete List By ID](actions/delete-list-by-id.md) | `DELETE /api/v1/list/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [delete meeting .](actions/delete-meeting.md) | `DELETE /api/v1/meeting/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete multiple communications.](actions/delete-multiple-communications.md) | `POST /api/v1/communication/multiple-delete` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete page](actions/delete-page.md) | `DELETE /api/v1/page/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete project by id](actions/delete-project-by-id.md) | `DELETE /api/v1/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Project Role By Role Id](actions/delete-project-role-by-role-id.md) | `DELETE /api/v1/project-role/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Release](actions/delete-release.md) | `DELETE /api/v1/release/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete spents](actions/delete-spents.md) | `DELETE /api/v1/task/spents/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Sprint By Sprint Id](actions/delete-sprint-by-sprint-id.md) | `DELETE /api/v1/sprint/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete task](actions/delete-task.md) | `DELETE /api/v1/task/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Team](actions/delete-team.md) | `DELETE /api/v1/team/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete WhiteBoard](actions/delete-white-board.md) | `DELETE /api/v1/white-board/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Widget By Widget Id](actions/delete-widget-by-widget-id.md) | `DELETE /api/v1/dashboard/widget/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete workspace roles by role ID](actions/delete-workspace-roles-by-role-id.md) | `DELETE /api/v1/workspace-role/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Download document by document ID](actions/download-document-by-document-id.md) | `GET /api/v1/document/all/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Drag form Element](actions/drag-form-element.md) | `POST /api/v1/form/element/position` | [docs](https://api.kitesuite.com/swagger/) |
| [Drag page](actions/drag-page.md) | `POST /api/v1/page/drag` | [docs](https://api.kitesuite.com/swagger/) |
| [drag widget](actions/drag-widget.md) | `PATCH /api/v1/dashboard/drag-widget/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Duplicate Page](actions/duplicate-page.md) | `POST /api/v1/page/duplicate` | [docs](https://api.kitesuite.com/swagger/) |
| [Export All imports by projectID](actions/export-all-imports-by-project-id.md) | `GET /api/v1/import-export/list/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Export All task by projectID](actions/export-all-task-by-project-id.md) | `GET /api/v1/import-export/export/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [form submission](actions/form-submission.md) | `POST /api/v1/form/submission` | [docs](https://api.kitesuite.com/swagger/) |
| [Get a single automation condition by ID](actions/get-a-single-automation-condition-by-id.md) | `GET /api/v1/automation/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get all automation conditions](actions/get-all-automation-conditions.md) | `GET /api/v1/automation` | [docs](https://api.kitesuite.com/swagger/) |
| [Get all automation histories](actions/get-all-automation-histories.md) | `GET /api/v1/automation/history` | [docs](https://api.kitesuite.com/swagger/) |
| [Get all campaigns by workspace](actions/get-all-campaigns-by-workspace.md) | `GET /api/v1/campaign` | [docs](https://api.kitesuite.com/swagger/) |
| [Get all conversations media](actions/get-all-conversations-media.md) | `GET /api/v1/media/conversation/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get All Dashboard by User ID](actions/get-all-dashboard-by-user-id.md) | `GET /api/v1/dashboard/user/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get All Dashboard by Workspace ID](actions/get-all-dashboard-by-workspace-id.md) | `GET /api/v1/dashboard/workspace/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get All Default Project Roles](actions/get-all-default-project-roles.md) | `GET /api/v1/project-role` | [docs](https://api.kitesuite.com/swagger/) |
| [Get all Directories of workspace](actions/get-all-directories-of-workspace.md) | `GET /api/v1/directory` | [docs](https://api.kitesuite.com/swagger/) |
| [Get all documents of workspace](actions/get-all-documents-of-workspace.md) | `GET /api/v1/document` | [docs](https://api.kitesuite.com/swagger/) |
| [Get All epic by projectID](actions/get-all-epic-by-project-id.md) | `GET /api/v1/epic/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get All epic by project key](actions/get-all-epic-by-project-key.md) | `GET /api/v1/epic/project/key/:key` | [docs](https://api.kitesuite.com/swagger/) |
| [Get all project data by project Id](actions/get-all-project-data-by-project-id.md) | `GET /api/v1/project/all/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get all Sprint activity data by project Id](actions/get-all-sprint-activity-data-by-project-id.md) | `GET /api/v1/report/sprint/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get All sub task by project ID](actions/get-all-sub-task-by-project-id.md) | `GET /api/v1/task/sub-task/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get All task by project ID](actions/get-all-task-by-project-id.md) | `GET /api/v1/task/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get all workspace roles](actions/get-all-workspace-roles.md) | `GET /api/v1/workspace-role` | [docs](https://api.kitesuite.com/swagger/) |
| [Get campaign analytics](actions/get-campaign-analytics.md) | `GET /api/v1/campaign/analytics` | [docs](https://api.kitesuite.com/swagger/) |
| [Get campaign by ID](actions/get-campaign-by-id.md) | `GET /api/v1/campaign/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get campaigns by account ID](actions/get-campaigns-by-account-id.md) | `GET /api/v1/campaign/account/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get communication](actions/get-communication.md) | `GET /api/v1/communication` | [docs](https://api.kitesuite.com/swagger/) |
| [Get communications of a specific thread.](actions/get-communications-of-a-specific-thread.md) | `GET /api/v1/communication/email/thread/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get completed sprints by projectID.](actions/get-completed-sprints-by-project-id.md) | `GET /api/v1/sprint/completed/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get conversations](actions/get-conversations.md) | `GET /api/v1/conversation/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Dashboard By Dashboard ID](actions/get-dashboard-by-dashboard-id.md) | `GET /api/v1/dashboard/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Directory by Id](actions/get-directory-by-id.md) | `GET /api/v1/directory/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get document by document ID](actions/get-document-by-document-id.md) | `GET /api/v1/document/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get document by search](actions/get-document-by-search.md) | `GET /api/v1/document/search/query` | [docs](https://api.kitesuite.com/swagger/) |
| [Get documents by project ID](actions/get-documents-by-project-id.md) | `GET /api/v1/document/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get form by form ID](actions/get-form-by-form-id.md) | `GET /api/v1/form/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get form by public key](actions/get-form-by-public-key.md) | `GET /api/v1/form/public/:publicKey` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Form Element by ID](actions/get-form-element-by-id.md) | `GET /api/v1/form/element/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Form Integrations by Form ID](actions/get-form-integrations-by-form-id.md) | `GET /api/v1/form/integrations/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Form Theme Templates](actions/get-form-theme-templates.md) | `GET /api/v1/form-theme` | [docs](https://api.kitesuite.com/swagger/) |
| [Get forms by project ID](actions/get-forms-by-project-id.md) | `GET /api/v1/form/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Gantt chart by project ID](actions/get-gantt-chart-by-project-id.md) | `GET /api/v1/gantt/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Invoice Preview](actions/get-invoice-preview.md) | `GET /api/v1/form/invoice/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get List By Project ID](actions/get-list-by-project-id.md) | `GET /api/v1/list/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Meeting.](actions/get-meeting.md) | `GET /api/v1/meeting/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get messages based on pagination](actions/get-messages-based-on-pagination.md) | `GET /api/v1/chat/conversation/:id?limit=10?page=1` | [docs](https://api.kitesuite.com/swagger/) |
| [Get notification by user Id](actions/get-notification-by-user-id.md) | `GET /api/v1/notification/user/:id?limit=5` | [docs](https://api.kitesuite.com/swagger/) |
| [Get page by page ID](actions/get-page-by-page-id.md) | `GET /api/v1/page/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get page history](actions/get-page-history.md) | `GET /api/v1/history/page/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Plan](actions/get-plan.md) | `GET /api/v1/plan` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Plan By ID](actions/get-plan-by-id.md) | `GET /api/v1/plan/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Predefined Field](actions/get-predefined-field.md) | `GET /api/v1/predefined-field` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Predefined Fields by project Id](actions/get-predefined-fields-by-project-id.md) | `GET /api/v1/predefined-field/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get project by Id](actions/get-project-by-id.md) | `GET /api/v1/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get project list fields.](actions/get-project-list-fields.md) | `GET /api/v1/project/list-fields/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Project Roles By Project ID](actions/get-project-roles-by-project-id.md) | `GET /api/v1/project-role/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Project Roles By User ID](actions/get-project-roles-by-user-id.md) | `GET /api/v1/project-role/user/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get projects by owner Id](actions/get-projects-by-owner-id.md) | `GET /api/v1/project/owner` | [docs](https://api.kitesuite.com/swagger/) |
| [Get projects by ProjectLeader Id](actions/get-projects-by-project-leader-id.md) | `GET /api/v1/project/projectLead/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get projects,lists,epics by workspace Id](actions/get-projectslistsepics-by-workspace-id.md) | `GET /api/v1/project/mobile/workspace/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get projects,lists,sprints,epics by workspace Id](actions/get-projectslistssprintsepics-by-workspace-id.md) | `GET /api/v1/project/workspace/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Public Document by ID](actions/get-public-document-by-id.md) | `GET /api/v1/document/public/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Release by Id](actions/get-release-by-id.md) | `GET /api/v1/release/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Release by project Id](actions/get-release-by-project-id.md) | `GET /api/v1/release/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get specified report data by projectId](actions/get-specified-report-data-by-project-id.md) | `GET /api/v1/report/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get sprint by ID.](actions/get-sprint-by-id.md) | `GET /api/v1/sprint/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get sprints by project ID](actions/get-sprints-by-project-id.md) | `GET /api/v1/sprint/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get task by assignee ID](actions/get-task-by-assignee-id.md) | `GET /api/v1/task/assignee/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get task by serial number.](actions/get-task-by-serial-number.md) | `GET /api/v1/task/sn/:sn?key=` | [docs](https://api.kitesuite.com/swagger/) |
| [Get task by task ID](actions/get-task-by-task-id.md) | `GET /api/v1/task/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Team by Id](actions/get-team-by-id.md) | `GET /api/v1/team/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get trash task by ID](actions/get-trash-task-by-id.md) | `GET /api/v1/task/trash/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get trashed project lists.](actions/get-trashed-project-lists.md) | `GET /api/v1/project/trashed` | [docs](https://api.kitesuite.com/swagger/) |
| [Get User By Id](actions/get-user-by-id-get-api-v1-user-id.md) | `GET /api/v1/user/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get User By workspace ID](actions/get-user-by-workspace-idget-api-v1-user-workspace-id.md) | `GET /api/v1/user/workspace/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get user's meeting in current workspace.](actions/get-users-meeting-in-current-workspace.md) | `GET /api/v1/meeting/workspace` | [docs](https://api.kitesuite.com/swagger/) |
| [Get WhiteBoard by Id](actions/get-white-board-by-id.md) | `GET /api/v1/white-board/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get WhiteBoard by project Id](actions/get-white-board-by-project-id.md) | `GET /api/v1/white-board/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Whiteboard Public URL](actions/get-whiteboard-public-url.md) | `GET /api/v1/white-board/public/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Workspace](actions/get-workspace.md) | `GET /api/v1/workspace/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [get workspace backup](actions/get-workspace-backup.md) | `GET /api/v1/import-export/backup` | [docs](https://api.kitesuite.com/swagger/) |
| [Get workspace forms](actions/get-workspace-forms.md) | `GET /api/v1/form` | [docs](https://api.kitesuite.com/swagger/) |
| [Get workspace roles by tenant ID](actions/get-workspace-roles-by-tenant-id.md) | `GET /api/v1/workspace-role/tenant/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get workspaces by user ID](actions/get-workspaces-by-user-id.md) | `GET /api/v1/workspace/user/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Import from Clickup](actions/import-from-clickup.md) | `POST /api/v1/import-export/import/clickup` | [docs](https://api.kitesuite.com/swagger/) |
| [Import from CSV](actions/import-from-csv.md) | `POST /api/v1/import-export/csv` | [docs](https://api.kitesuite.com/swagger/) |
| [Import From Jira](actions/import-from-jira.md) | `POST /api/v1/import-export/import/jira` | [docs](https://api.kitesuite.com/swagger/) |
| [List Teams](actions/list-teams.md) | `GET /api/v1/team` | [docs](https://api.kitesuite.com/swagger/) |
| [move List position](actions/move-list-position.md) | `POST /api/v1/list/position` | [docs](https://api.kitesuite.com/swagger/) |
| [Move page to another document](actions/move-page-to-another-document.md) | `POST /api/v1/page/move` | [docs](https://api.kitesuite.com/swagger/) |
| [move task](actions/move-task.md) | `POST /api/v1/task/move` | [docs](https://api.kitesuite.com/swagger/) |
| [Redeem Coupon](actions/redeem-coupon.md) | `POST /api/v1/form/coupon/redeem` | [docs](https://api.kitesuite.com/swagger/) |
| [Remove Form Integration](actions/remove-form-integration.md) | `DELETE /api/v1/form/integration/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Remove member from project.](actions/remove-member-from-project.md) | `DELETE /api/v1/project/member/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Remove member in workspace.](actions/remove-member-in-workspace.md) | `DELETE /api/v1/workspace/member/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [remove Whiteboard Objects](actions/remove-whiteboard-objects.md) | `POST /api/v1/white-board/object/remove` | [docs](https://api.kitesuite.com/swagger/) |
| [Reorder child issue](actions/reorder-child-issue.md) | `PATCH /api/v1/epic/task/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Reorder sub task by sub task Id](actions/reorder-sub-task-by-sub-task-id.md) | `PATCH /api/v1/task/sub-task/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Reset default custom Field by project Id](actions/reset-default-custom-field-by-project-id.md) | `PATCH /api/v1/custom-field/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Restore document](actions/restore-document.md) | `PATCH /api/v1/document/restore/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Restore project](actions/restore-project.md) | `POST /api/v1/project/restore` | [docs](https://api.kitesuite.com/swagger/) |
| [Search All Data in Workspace](actions/search-all-data-in-workspace.md) | `GET /api/v1/workspace/search/:query` | [docs](https://api.kitesuite.com/swagger/) |
| [Send Email through app](actions/send-email-through-app.md) | `POST /api/v1/communication/email` | [docs](https://api.kitesuite.com/swagger/) |
| [sync data by project Id](actions/sync-data-by-project-id.md) | `POST /api/v1/report/timesheet` | [docs](https://api.kitesuite.com/swagger/) |
| [Sync directory](actions/sync-directory.md) | `POST /api/v1/directory/sync` | [docs](https://api.kitesuite.com/swagger/) |
| [Track email link clicks and redirect to the target link.](actions/track-email-link-clicks-and-redirect-to-the-target-link.md) | `GET /api/v1/communication/link/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Track email open status through a tracking pixel.](actions/track-email-open-status-through-a-tracking-pixel.md) | `GET /api/v1/communication/email/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Undo Whiteboard Object Deletion](actions/undo-whiteboard-object-deletion.md) | `PATCH /api/v1/white-board/object/undo-redo` | [docs](https://api.kitesuite.com/swagger/) |
| [Unsubscribe from communication emails.](actions/unsubscribe-from-communication-emails.md) | `GET /api/v1/communication/unsubscribe/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update a campaign by its ID](actions/update-a-campaign-by-its-id.md) | `PATCH /api/v1/campaign/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update a schedule by ID](actions/update-a-schedule-by-id.md) | `PATCH /api/v1/campaign/schedule/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update a sequence by ID](actions/update-a-sequence-by-id.md) | `PATCH /api/v1/campaign/sequence/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update a single automation condition by ID](actions/update-a-single-automation-condition-by-id.md) | `PATCH /api/v1/automation/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update communication](actions/update-communication.md) | `POST /api/v1/communication/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Coupon](actions/update-coupon.md) | `PATCH /api/v1/form/coupon/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update custom Field by Id](actions/update-custom-field-by-id.md) | `PATCH /api/v1/custom-field/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Dashboard](actions/update-dashboard.md) | `PATCH /api/v1/dashboard/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Directory](actions/update-directory.md) | `PATCH /api/v1/directory/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update document](actions/update-document.md) | `PATCH /api/v1/document/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Epic](actions/update-epic.md) | `PATCH /api/v1/epic/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Field by Id](actions/update-field-by-id.md) | `PATCH /api/v1/check-list/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update form](actions/update-form.md) | `PATCH /api/v1/form/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Form Condition](actions/update-form-condition.md) | `PATCH /api/v1/form/condition/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Form Design](actions/update-form-design.md) | `PATCH /api/v1/form-design/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Form Dropbox Action](actions/update-form-dropbox-action.md) | `PATCH /api/v1/form/integration/dropbox/actions/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update form Element](actions/update-form-element.md) | `PATCH /api/v1/form/element/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Form Google Calendar Event](actions/update-form-google-calendar-event.md) | `PATCH /api/v1/form/integration/google-calendar/events/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Form Google Drive Action](actions/update-form-google-drive-action.md) | `PATCH /api/v1/form/integration/google-drive/actions/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Form Google Sheets Integration](actions/update-form-google-sheets-integration.md) | `PATCH /api/v1/form/integration/google-sheet/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Form Mailchimp Integration](actions/update-form-mailchimp-integration.md) | `PATCH /api/v1/form/integration/mailchimp/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Form OneDrive Action](actions/update-form-one-drive-action.md) | `PATCH /api/v1/form/integration/one-drive/actions/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Form payment](actions/update-form-payment.md) | `PATCH /api/v1/form/payment/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Form Salesforce Action](actions/update-form-salesforce-action.md) | `PATCH /api/v1/form/integration/salesforce/actions/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [update form submission](actions/update-form-submission.md) | `POST /api/v1/form/public/submission/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Form Thank You Page](actions/update-form-thank-you-page.md) | `PATCH /api/v1/form-ty/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update label from project.](actions/update-label-from-project.md) | `PATCH /api/v1/label/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [update meeting .](actions/update-meeting.md) | `PATCH /api/v1/meeting/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update member's role to project.](actions/update-members-role-to-project.md) | `PATCH /api/v1/project/member/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update multiple document](actions/update-multiple-document.md) | `POST /api/v1/document/multiple` | [docs](https://api.kitesuite.com/swagger/) |
| [Update multiple members in workspace.](actions/update-multiple-members-in-workspace.md) | `POST /api/v1/workspace/member/multiple` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Multiple Members to project.](actions/update-multiple-members-to-project.md) | `POST /api/v1/project/member/multiple` | [docs](https://api.kitesuite.com/swagger/) |
| [update multiple tasks](actions/update-multiple-tasks.md) | `POST /api/v1/task/multiple` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Multiple Whiteboard Objects](actions/update-multiple-whiteboard-objects.md) | `POST /api/v1/white-board/object/multiple` | [docs](https://api.kitesuite.com/swagger/) |
| [Update notification of user](actions/update-notification-of-user.md) | `PATCH /api/v1/notification/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update page](actions/update-page.md) | `PATCH /api/v1/page/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update predefined Field](actions/update-predefined-field.md) | `PATCH /api/v1/predefined-field/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Product Position in Form Element](actions/update-product-position-in-form-element.md) | `PUT /api/v1/form/element/product/position/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Project](actions/update-project.md) | `PUT /api/v1/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update project list fields.](actions/update-project-list-fields.md) | `PATCH /api/v1/project/list-fields/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Release](actions/update-release.md) | `PATCH /api/v1/release/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Role](actions/update-role.md) | `PUT /api/v1/project-role/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update role in workspace by workspace Id.](actions/update-role-in-workspace-by-workspace-id.md) | `PATCH /api/v1/workspace/member/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Sprint](actions/update-sprint.md) | `PUT /api/v1/sprint/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [update submission](actions/update-submission.md) | `PUT /api/v1/form/submission/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update task by Id](actions/update-task-by-id.md) | `PATCH /api/v1/task/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update task List from one to another](actions/update-task-list-from-one-to-another.md) | `PATCH /api/v1/list/task/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Tasks in sprint](actions/update-tasks-in-sprint.md) | `POST /api/v1/sprint/task` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Team](actions/update-team.md) | `PATCH /api/v1/team/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update the ListName](actions/update-the-list-name.md) | `PATCH /api/v1/list/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update User Avatar By ID](actions/update-user-avatar-by-idpatch-api-v1-user-avatar-id.md) | `PATCH /api/v1/user/avatar/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update User By ID](actions/update-user-by-idpatch-api-v1-user-id.md) | `PATCH /api/v1/user/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update WhiteBoard](actions/update-white-board.md) | `PATCH /api/v1/white-board/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Whiteboard Object](actions/update-whiteboard-object.md) | `PATCH /api/v1/white-board/object/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Whiteboard Object Position](actions/update-whiteboard-object-position.md) | `POST /api/v1/white-board/object/position` | [docs](https://api.kitesuite.com/swagger/) |
| [update widget](actions/update-widget.md) | `PATCH /api/v1/dashboard/widget/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update workspace](actions/update-workspace.md) | `PATCH /api/v1/workspace/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Workspace Avatar](actions/update-workspace-avatar.md) | `PATCH /api/v1/workspace/avatar/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update workspace roles by role ID](actions/update-workspace-roles-by-role-id.md) | `PATCH /api/v1/workspace-role/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Upload Attachment](actions/upload-attachment.md) | `POST /api/v1/media/upload` | [docs](https://api.kitesuite.com/swagger/) |
| [Upload Epic Attachment](actions/upload-epic-attachment.md) | `POST /api/v1/epic/upload` | [docs](https://api.kitesuite.com/swagger/) |
| [Upload form Attachment](actions/upload-form-attachment.md) | `POST /api/v1/media/form/upload` | [docs](https://api.kitesuite.com/swagger/) |
| [Upload workspace Attachment](actions/upload-workspace-attachment.md) | `POST /api/v1/media/worksapce/upload` | [docs](https://api.kitesuite.com/swagger/) |
