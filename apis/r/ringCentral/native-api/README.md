# RingCentral: Native API Reference

A consolidated summary of RingCentral's API configuration and 15 documented operations.

- **API base URL:** `https://platform.ringcentral.com/`

## Authentication

### OAuth 2.0

### Credentials

- **Client ID:** `clientId` · required · Create a private RingCentral app and paste its Client ID here.
- **Client Secret:** `clientSecret` · required · Create a private RingCentral app and paste its Client Secret here.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://platform.ringcentral.com/restapi/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://platform.ringcentral.com/restapi/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://platform.ringcentral.com/restapi/oauth/token.

[Official authentication documentation](https://developers.ringcentral.com/guide/authentication/auth-code-flow)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

Use `perPage` in the query string to set the page size (default 50; accepted range 1–1000). Use `page` in the query string as the pagination cursor; numbering starts at 1. Follow the complete next-page URL returned by the API.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Message](actions/delete-message.md) | `DELETE restapi/v1.0/account/:accountId/extension/:extensionId/message-store/:messageId` | [docs](https://developers.ringcentral.com/api-reference/Message-Store/deleteMessage) |
| [Get Account Info](actions/get-account-info.md) | `GET restapi/v1.0/account/~` | [docs](https://developers.ringcentral.com/api-reference/Company/getAccountInfoV2) |
| [Get Call Queue](actions/get-call-queue.md) | `GET restapi/v1.0/account/:accountId/call-queues/:groupId` | [docs](https://developers.ringcentral.com/api-reference/Call-Queues/readCallQueueInfo) |
| [Get Call Recording](actions/get-call-recording.md) | `GET restapi/v1.0/account/:accountId/recording/:recordingId` | [docs](https://developers.ringcentral.com/api-reference/Call-Recordings/readCallRecording) |
| [Get Call Recording Content](actions/get-call-recording-content.md) | `GET restapi/v1.0/account/:accountId/recording/:recordingId/content` | [docs](https://developers.ringcentral.com/api-reference/Call-Recordings/readCallRecording) |
| [Get Extension](actions/get-extension.md) | `GET restapi/v1.0/account/:accountId/extension/:extensionId` | [docs](https://developers.ringcentral.com/api-reference/User-Settings/readExtension) |
| [Get Message](actions/get-message.md) | `GET restapi/v1.0/account/:accountId/extension/:extensionId/message-store/:messageId` | [docs](https://developers.ringcentral.com/api-reference/Message-Store/readMessage) |
| [List Call Queues](actions/list-call-queues.md) | `GET restapi/v1.0/account/:accountId/call-queues` | [docs](https://developers.ringcentral.com/api-reference/Call-Queues/listCallQueues) |
| [List Company Call Records](actions/list-company-call-records.md) | `GET restapi/v1.0/account/:accountId/call-log` | [docs](https://developers.ringcentral.com/api-reference/Call-Log/readCompanyCallLog) |
| [List Company Phone Numbers](actions/list-company-phone-numbers.md) | `GET restapi/v1.0/account/:accountId/phone-number` | [docs](https://developers.ringcentral.com/api-reference/Phone-Numbers/listAccountPhoneNumbers) |
| [List Extension Phone Numbers](actions/list-extension-phone-numbers.md) | `GET restapi/v1.0/account/:accountId/extension/:extensionId/phone-number` | [docs](https://developers.ringcentral.com/api-reference/Phone-Numbers/listExtensionPhoneNumbers) |
| [List Extensions](actions/list-extensions.md) | `GET restapi/v1.0/account/:accountId/extension` | [docs](https://developers.ringcentral.com/api-reference/Extensions/listExtensions) |
| [List Messages](actions/list-messages.md) | `GET restapi/v1.0/account/:accountId/extension/:extensionId/message-store` | [docs](https://developers.ringcentral.com/api-reference/Message-Store/listMessages) |
| [List User Call Records](actions/list-user-call-records.md) | `GET restapi/v1.0/account/:accountId/extension/:extensionId/call-log` | [docs](https://developers.ringcentral.com/api-reference/Call-Log/readCompanyCallLog) |
| [Send SMS](actions/send-sms.md) | `POST restapi/v1.0/account/:accountId/extension/:extensionId/sms` | [docs](https://developers.ringcentral.com/api-reference/SMS/createSMSMessage) |
