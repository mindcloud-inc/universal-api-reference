# FuseDesk: Native API Reference

A consolidated summary of FuseDesk's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.fusedesk.com/api/
- **API base URL:** `https://{appName}.fusedesk.com`

## Authentication

### API Key

Authenticate with a FuseDesk API key from Settings.

### Credentials

- **API Key:** `apiKey` · required
- **App Name:** `appName` · required · Your FuseDesk app name from https://YOURAPPNAME.fusedesk.com, for example mindcloud

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.fusedesk.com/api/)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Case Note](actions/add-case-note.md) | `POST /api/v1/cases/:caseId/addnote` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#148b96a5-d816-41d4-ad33-a29642287c85) |
| [Apply Case Tag](actions/apply-case-tag.md) | `POST /api/v1/cases/:caseId/tag/:caseTagId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#5afd2da9-d6c8-41ee-b93b-41b0d5ddd7bc) |
| [Archive Department](actions/archive-department.md) | `DELETE /api/v2/departments/:departmentId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#8f716acb-8b49-422e-831b-57f39e737f86) |
| [Bulk Update Cases](actions/bulk-update-cases.md) | `POST /api/v1/cases/update` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#be7213cd-a217-4953-9090-7095216f3356) |
| [Close Chat](actions/close-chat.md) | `POST /api/v1/chats/:chatId/close` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#fda44692-6a99-4b38-8d98-408bdbeca27f) |
| [Create Case](actions/create-case.md) | `POST /api/v1/cases` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#760ba74c-07f2-4f43-a057-b0417d12e694) |
| [Create Case Tag](actions/create-case-tag.md) | `POST /api/v1/casetags` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#05f9241b-de05-4355-960e-74c194639017) |
| [Create Contact](actions/create-contact.md) | `POST /api/v2/contacts` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#39b23fd9-d985-4daa-bc3e-ba60e20eee95) |
| [Create Department](actions/create-department.md) | `POST /api/v2/departments` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#3d38c890-4ef6-4de7-8dc1-92395a3ed813) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/v2/webhooks` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#74bd4635-69aa-477c-8ba8-dbe07422af4e) |
| [Delete Case Tag](actions/delete-case-tag.md) | `DELETE /api/v1/casetags/:caseTagId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#c1ae161d-bdad-40bc-9ac8-e1d28bd9f931) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/v2/webhooks/:webhookId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#35aa02a4-9eaa-4194-a092-32959f5462e5) |
| [Disable Case Feedback](actions/disable-case-feedback.md) | `POST /api/v1/cases/:caseId/feedback/dontask` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#de345295-df28-4851-a914-ff3d6ec3216b) |
| [Enable Case Feedback](actions/enable-case-feedback.md) | `POST /api/v1/cases/:caseId/feedback/doask` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#b55af1e9-0f7d-475d-bc38-0c72a6adc0b5) |
| [Get Case](actions/get-case.md) | `GET /api/v1/cases/:caseId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#7fab000b-8f38-440c-bfa9-c9630e9af8c2) |
| [Get Case Feedback Data](actions/get-case-feedback-data.md) | `GET /api/v1/cases/:caseId/feedback` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#5d926fba-764f-45b4-aaff-e961cc84efee) |
| [Get Chat](actions/get-chat.md) | `GET /api/v1/chats/:chatId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#b5ca8abc-a274-4bae-9ca3-f04735e0fe72) |
| [Get Contact](actions/get-contact.md) | `GET /api/v2/contacts/:contactId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#bd3381b3-f9e7-47eb-a516-f30756c55473) |
| [Get Department](actions/get-department.md) | `GET /api/v2/departments/:departmentId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#5f33b697-31eb-4ee1-8172-e8469a98a5d7) |
| [Get Email](actions/get-email.md) | `GET /api/v1/emails/:emailId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#7ad42157-6c3f-4962-bf2e-8aebbb4bb5bc) |
| [Get Rep](actions/get-rep.md) | `GET /api/v2/reps/:userId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#dd2745a5-1205-4043-b00a-324d7aff1b4f) |
| [List Active Departments](actions/list-active-departments.md) | `GET /api/v2/departments` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#0c956f60-09e1-4cce-9a74-8ed477a786e2) |
| [List All Departments](actions/list-all-departments.md) | `GET /api/v2/departments/all` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#6ce5c727-d6c9-470a-b9c7-179ee85e123f) |
| [List Archived Departments](actions/list-archived-departments.md) | `GET /api/v2/departments/archived` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#05e66073-09b6-48ac-a341-89c2122b0002) |
| [List Case Tags](actions/list-case-tags.md) | `GET /api/v1/casetags` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#11e964aa-3203-4a83-92cb-42c79a682380) |
| [List Chats](actions/list-chats.md) | `GET /api/v1/chats` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#28be6359-388d-4743-8d2c-f0009cb627ac) |
| [List Reps](actions/list-reps.md) | `GET /api/v2/reps` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#c90bfd4d-9356-4f30-926d-38df875f1fab) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/v2/webhooks` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#e9fb9adb-726f-4af1-9f77-ad06f344c82a) |
| [Remove Case Tag](actions/remove-case-tag.md) | `POST /api/v1/cases/:caseId/untag/:caseTagId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#f906c62f-77b0-4d26-bd9e-5047d7db8395) |
| [Reply to Case by Email](actions/reply-to-case-by-email.md) | `POST /api/v1/cases/:caseId/reply` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#209dae86-c3c5-404c-aaea-d21e9c551b45) |
| [Request Case Feedback Now](actions/request-case-feedback-now.md) | `POST /api/v1/cases/:caseId/feedback/request` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#796c2bc2-1efc-48d3-abfa-be6ead9045c5) |
| [Restore Archived Department](actions/restore-archived-department.md) | `POST /api/v2/departments/:departmentId/restore` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#812e436f-6c89-430e-8ebc-35c3caff62d9) |
| [Search Cases](actions/search-cases.md) | `GET /api/v1/cases` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#312f3a20-e8bb-4bff-a73e-b9d075ced263) |
| [Search Contacts](actions/search-contacts.md) | `GET /api/v2/contacts` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#77197b55-cc58-4087-b0da-c1f449292d8f) |
| [Search Emails](actions/search-emails.md) | `GET /api/v1/emails/unassigned` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#769f8f25-7063-4f31-8646-82fbd211b994) |
| [Snooze Case](actions/snooze-case.md) | `POST /api/v1/cases/:caseId/snooze` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#ba5d9b6a-2cb6-4d74-a798-a69baaa9ce27) |
| [Update Case](actions/update-case.md) | `POST /api/v1/cases/:caseId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#62bfa40e-747e-4b05-97cf-c15e84ffe55d) |
| [Update Chat](actions/update-chat.md) | `POST /api/v1/chats/:chatId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#04842f72-4833-46c1-bd1a-b4213a0e008d) |
| [Update Contact](actions/update-contact.md) | `POST /api/v2/contacts/:contactId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#17df2743-b569-4e07-9e5a-85ce25bae6d4) |
| [Update Department](actions/update-department.md) | `POST /api/v2/departments/:departmentId` | [docs](https://documenter.getpostman.com/view/11014835/SztBc8ix#56fca54b-34af-4d3d-9eb5-b5055401b4ac) |
