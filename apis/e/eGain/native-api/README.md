# eGain: Native API Reference

A consolidated summary of eGain's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://apidev.egain.com/api-catalog/conversation-conversationmgr/api-bundled/overview/
- **OpenAPI specification:** https://apidev.egain.com/_bundle/apis/v3/conversation/conversationmgr/api-bundled.yaml
- **API base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`

## Authentication

### OAuth2

Use an eGain client application with server-to-server OAuth2 credentials. The tenant-specific token URL must come from the eGain client application's Metadata panel.

### Credentials

- **Token URL:** `tokenUrl` · required · Exact tenant-specific OAuth2 token URL copied from the eGain client application's Metadata panel.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to {{credentials.tokenUrl}}.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `app.conversation.conversationmgr.read app.conversation.conversationmgr.manage`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://apidev.egain.com/developer-portal/get-started/authentication_guide)

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/account/createaccount.md) |
| [Create Asset](actions/create-asset.md) | `POST /assets` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/assets/createasset.md) |
| [Create Authentication](actions/create-authentication.md) | `POST /authentications` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/authentication/createauthentication.md) |
| [Create Channel](actions/create-channel.md) | `POST /channels` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/channel/createchannel.md) |
| [Create Client Application](actions/create-client-application.md) | `POST /clientapplications` | [docs](https://apidev.egain.com/api-catalog/conversation-conversationmgr/api-bundled/operation/createClientApplication/) |
| [Create Orchestration](actions/create-orchestration.md) | `POST /orchestrations` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/orchestration/createorchestration.md) |
| [Create Participant](actions/create-participant.md) | `POST /participants` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/participant/createparticipant.md) |
| [Delete Account](actions/delete-account.md) | `DELETE /accounts/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/account/deleteaccount.md) |
| [Delete Asset](actions/delete-asset.md) | `DELETE /assets/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/assets/deleteasset.md) |
| [Delete Authentication](actions/delete-authentication.md) | `DELETE /authentications/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/authentication/deleteauthentication.md) |
| [Delete Channel](actions/delete-channel.md) | `DELETE /channels/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/channel/deletechannel.md) |
| [Delete Client Application](actions/delete-client-application.md) | `DELETE /clientapplications/:id` | [docs](https://apidev.egain.com/api-catalog/conversation-conversationmgr/api-bundled/operation/deleteClientApplication/) |
| [Delete Orchestration](actions/delete-orchestration.md) | `DELETE /orchestrations/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/orchestration/deleteorchestration.md) |
| [Delete Participant](actions/delete-participant.md) | `DELETE /participants/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/participant/deleteparticipant.md) |
| [Get Account](actions/get-account.md) | `GET /accounts/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/account/getaccount.md) |
| [Get Asset](actions/get-asset.md) | `GET /assets/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/assets/getasset.md) |
| [Get Authentication](actions/get-authentication.md) | `GET /authentications/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/authentication/getauthentication.md) |
| [Get Channel](actions/get-channel.md) | `GET /channels/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/channel/getchannel.md) |
| [Get Client Application](actions/get-client-application.md) | `GET /clientapplications/:id` | [docs](https://apidev.egain.com/api-catalog/conversation-conversationmgr/api-bundled/operation/getClientApplication/) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/conversation/fetchconversation.md) |
| [Get Orchestration](actions/get-orchestration.md) | `GET /orchestrations/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/orchestration/getorchestration.md) |
| [Get Participant](actions/get-participant.md) | `GET /participants/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/participant/getparticipant.md) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/account/getallaccounts.md) |
| [List Authentications](actions/list-authentications.md) | `GET /authentications` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/authentication/getallauthentication.md) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/channel/getallchannels.md) |
| [List Client Applications](actions/list-client-applications.md) | `GET /clientapplications` | [docs](https://apidev.egain.com/api-catalog/conversation-conversationmgr/api-bundled/operation/getAllClientApplication/) |
| [List Orchestrations](actions/list-orchestrations.md) | `GET /orchestrations` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/orchestration/getallorchestration.md) |
| [List Participants](actions/list-participants.md) | `GET /participants` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/participant/getallparticipant.md) |
| [Send Message](actions/send-message.md) | `POST /conversations/messages` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/conversation/sendmessage.md) |
| [Update Account](actions/update-account.md) | `PUT /accounts/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/account/updateaccount.md) |
| [Update Authentication](actions/update-authentication.md) | `PUT /authentications/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/authentication/updateauthentication.md) |
| [Update Channel](actions/update-channel.md) | `PUT /channels/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/channel/updatechannel.md) |
| [Update Client Application](actions/update-client-application.md) | `PUT /clientapplications/:id` | [docs](https://apidev.egain.com/api-catalog/conversation-conversationmgr/api-bundled/operation/updateClientApplication/) |
| [Update Orchestration](actions/update-orchestration.md) | `PUT /orchestrations/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/orchestration/updateorchestration.md) |
| [Update Participant](actions/update-participant.md) | `PUT /participants/:id` | [docs](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/participant/updateparticipant.md) |
