# MindMe: Native API Reference

A consolidated summary of MindMe's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.mindmemobile.com/platform/app/
- **OpenAPI specification:** https://prodapi.mindmemobile.com/swagger/v1/swagger.json
- **API base URL:** `https://prodapi.mindmemobile.com`

## Authentication

### Access key authentication

Exchange a MindMe access key and secret for a bearer token.

### Credentials

- **Secret:** `secret` · required · MindMe secret used to obtain a bearer token.
- **Access Key:** `accessKey` · required · MindMe access key used to obtain a bearer token.

Send these headers with each API request:

```http
Authorization: Bearer <custom.Data.Token>
```

[Official authentication documentation](https://prodapi.mindmemobile.com/swagger/index.html)

## API conventions

Response data is read from `Data`.

## Pagination

Use `pageSize` in the query string to set the page size (default 10). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contacts To Sequence](actions/add-contacts-to-sequence.md) | `POST /api/Automation/AddContactsToSequence` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Automation~1AddContactsToSequence/post) |
| [Create Automation](actions/create-automation.md) | `POST /api/Automation/SaveAutomationSetting` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Automation~1SaveAutomationSetting/post) |
| [Create Campaign](actions/create-campaign.md) | `POST /api/Campaign/SaveCampaign` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Campaign~1SaveCampaign/post) |
| [Create Contact](actions/create-contact.md) | `POST /api/Contact/CreateNewContact` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Contact~1CreateNewContact/post) |
| [Create Contact List](actions/create-contact-list.md) | `POST /api/List/CreateList` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1List~1CreateList/post) |
| [Create Contact Note](actions/create-contact-note.md) | `POST /api/Contact/CreateContactNote` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Contact~1CreateContactNote/post) |
| [Create CRM Appointment](actions/create-crm-appointment.md) | `POST /api/CRM/SaveAppointment` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1CRM~1SaveAppointment/post) |
| [Create CRM Task](actions/create-crm-task.md) | `POST /api/CRM/CreateTask` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1CRM~1CreateTask/post) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /api/CustomFields/SaveCustomField` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1CustomFields~1SaveCustomField/post) |
| [Create Deal](actions/create-deal.md) | `POST /api/PipeLinesAndDeals/SaveDeal` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1PipeLinesAndDeals~1SaveDeal/post) |
| [Create Or Transfer Conversation](actions/create-or-transfer-conversation.md) | `POST /api/Conversation/CreateOrTransferConversation` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Conversation~1CreateOrTransferConversation/post) |
| [Create Smart List](actions/create-smart-list.md) | `POST /api/List/SaveSmartList` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1List~1SaveSmartList/post) |
| [Create Tag](actions/create-tag.md) | `POST /api/Tag/CreateTag` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Tag~1CreateTag/post) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /api/Contact/DeleteContact` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Contact~1DeleteContact/delete) |
| [Get Access Token](actions/get-access-token.md) | `POST /api/Account/GetAccessToken` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Account~1GetAccessToken/post) |
| [Get Campaign](actions/get-campaign.md) | `GET /api/Campaign/GetCampaignDetailByCampaignId` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Campaign~1GetCampaignDetailByCampaignId/get) |
| [Get Contact](actions/get-contact.md) | `GET /api/Contact/GetContactById` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Contact~1GetContactById/get) |
| [List Automations](actions/list-automations.md) | `POST /api/Automation/GetAutomationSummaryPagingWithFilter` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Automation~1GetAutomationSummaryPagingWithFilter/post) |
| [List Campaigns](actions/list-campaigns.md) | `GET /api/Campaign/GetCampaignSummaryByFilter` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Campaign~1GetCampaignSummaryByFilter/get) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /api/List/GetLists` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1List~1GetLists/get) |
| [List Contact Notes](actions/list-contact-notes.md) | `GET /api/Contact/GetContactNotes` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Contact~1GetContactNotes/get) |
| [List Contacts](actions/list-contacts.md) | `GET /api/Contact/GetContactByFilter` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Contact~1GetContactByFilter/get) |
| [List Contacts By List](actions/list-contacts-by-list.md) | `GET /api/List/GetContactsByList` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1List~1GetContactsByList/get) |
| [List Conversation Messages](actions/list-conversation-messages.md) | `GET /api/Conversation/GetConversationMessages` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Conversation~1GetConversationMessages/get) |
| [List Conversations](actions/list-conversations.md) | `GET /api/Conversation/FilterConversations` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Conversation~1FilterConversations/get) |
| [List CRM Calendar Activities](actions/list-crm-calendar-activities.md) | `GET /api/CRM/GetCRMCalendarActivities` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1CRM~1GetCRMCalendarActivities/get) |
| [List CRM Tasks](actions/list-crm-tasks.md) | `POST /api/CRM/GetTasksWithFilter` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1CRM~1GetTasksWithFilter/post) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /api/CustomFields/GetCustomFields` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1CustomFields~1GetCustomFields/get) |
| [List Deals](actions/list-deals.md) | `POST /api/PipeLinesAndDeals/GetDealsGridData` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1PipeLinesAndDeals~1GetDealsGridData/post) |
| [List Inboxes](actions/list-inboxes.md) | `GET /api/Conversation/GetInboxes` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Conversation~1GetInboxes/get) |
| [List Media Files](actions/list-media-files.md) | `GET /api/AccountMedia/GetMediaLibraryByFilter` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1AccountMedia~1GetMediaLibraryByFilter/get) |
| [List Tags](actions/list-tags.md) | `GET /api/Tag/GetAllTagsInSubAccounts` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Tag~1GetAllTagsInSubAccounts/get) |
| [List Time Zones](actions/list-time-zones.md) | `GET /api/TimeZone/GetAllTimeZones` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1TimeZone~1GetAllTimeZones/get) |
| [Send Conversation Message](actions/send-conversation-message.md) | `POST /api/Conversation/SendConversationMessage` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Conversation~1SendConversationMessage/post) |
| [Update Automation Status](actions/update-automation-status.md) | `POST /api/Automation/ChangeAutomationStatusById` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Automation~1ChangeAutomationStatusById/post) |
| [Update Campaign Routes](actions/update-campaign-routes.md) | `POST /api/Campaign/SaveCampaignRoutes` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Campaign~1SaveCampaignRoutes/post) |
| [Update Campaign Schedule](actions/update-campaign-schedule.md) | `POST /api/Campaign/SaveCampaignScheduling` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Campaign~1SaveCampaignScheduling/post) |
| [Update Contact](actions/update-contact.md) | `PUT /api/Contact/UpdateContact` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Contact~1UpdateContact/put) |
| [Update Contact Categories](actions/update-contact-categories.md) | `POST /api/Contact/AddOrRemoveContactsByCategories` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Contact~1AddOrRemoveContactsByCategories/post) |
| [Upload Media File](actions/upload-media-file.md) | `POST /api/AccountMedia/UploadMediaFile` | [docs](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1AccountMedia~1UploadMediaFile/post) |
