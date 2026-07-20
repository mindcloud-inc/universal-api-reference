# MailUp: Native API Reference

A consolidated summary of MailUp's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help
- **API base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://services.mailup.com/Authorization/OAuth/LogOn to approve access.
2. Exchange the returned authorization code with a POST request to https://services.mailup.com/Authorization/OAuth/Token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://services.mailup.com/Authorization/OAuth/Token.

[Official authentication documentation](https://helpmailup.atlassian.net/wiki/spaces/mailupapi/pages/450002975/AI_REST%2BAPI_Standard)

## API conventions

The current page number is read from `pageNumber`.

## Pagination

Use `pageSize` in the query string to set the page size. Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sortExpression` in the query string. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Email](actions/create-email.md) | `POST Console/List/:id_List/Email` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/CreateEmailMessage) |
| [Create Group](actions/create-group.md) | `POST Console/List/:id_List/Group` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/CreateGroup) |
| [Create List](actions/create-list.md) | `POST Console/List` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/CreateNewList) |
| [Get Authentication Details](actions/get-authentication-details.md) | `GET Console/Authentication/Details` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetConsoleAuthenticatedUserDetails) |
| [Get Authentication Info](actions/get-authentication-info.md) | `GET Console/Authentication/Info` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetConsoleAuthenticatedUserInfo) |
| [Get Email](actions/get-email.md) | `GET Console/List/:id_List/Email/:id_Message` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetMessageDetails) |
| [Get Email Send History](actions/get-email-send-history.md) | `GET Console/List/:id_List/Email/:id_Message/SendHistory` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetMailMessageSendHistory) |
| [Get Import](actions/get-import.md) | `GET Console/Imports/:id_Import` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetImportDetailsByIdImport) |
| [Get List](actions/get-list.md) | `GET Console/List/:id_List` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetExistingListById) |
| [Import Recipient](actions/import-recipient.md) | `POST Console/List/:id_List/Recipient` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/AsyncImportRecipientToList) |
| [Import Recipients](actions/import-recipients.md) | `POST Console/List/:id_List/Recipients` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/AsyncImportRecipientsToList) |
| [List Emails](actions/list-emails.md) | `GET Console/List/:id_List/Emails` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetMailMessagesByList) |
| [List Groups](actions/list-groups.md) | `GET Console/List/:id_List/Groups` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetConsoleGroupsByList) |
| [List Imports](actions/list-imports.md) | `GET Console/Imports` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetImports) |
| [List Lists](actions/list-lists.md) | `GET Console/List` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetExistingLists) |
| [List Pending Recipients](actions/list-pending-recipients.md) | `GET Console/List/:id_List/Recipients/Pending` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetPendingRecipientsByList) |
| [List Recipient Opt-ins](actions/list-recipient-opt-ins.md) | `GET Console/List/:id_List/Recipients/EmailOptins` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/EmailOptins) |
| [List Subscribed Recipients](actions/list-subscribed-recipients.md) | `GET Console/List/:id_List/Recipients/Subscribed` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetSubscribedRecipientsByList) |
| [List Unsubscribed Recipients](actions/list-unsubscribed-recipients.md) | `GET Console/List/:id_List/Recipients/Unsubscribed` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetUnsubscribedRecipientsByList) |
| [Send Email](actions/send-email.md) | `POST Console/List/:id_List/Email/:id_Message/Send` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/SendMailMessageToRecipientInList) |
| [Subscribe Recipient](actions/subscribe-recipient.md) | `POST Console/List/:id_List/Subscribe/:id_Recipient` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/SubscribeRecipientToList) |
| [Unsubscribe Recipient](actions/unsubscribe-recipient.md) | `DELETE Console/List/:id_List/Unsubscribe/:id_Recipient` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/RemoveRecipientFromList) |
| [Update Email](actions/update-email.md) | `PUT Console/List/:id_List/Email/:id_Message` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/UpdateEmailMessage) |
| [Update List](actions/update-list.md) | `PUT Console/List/:id_List` | [docs](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/UpdateExistingList) |
