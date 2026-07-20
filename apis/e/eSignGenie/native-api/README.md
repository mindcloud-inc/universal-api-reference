# eSign Genie: Native API Reference

A consolidated summary of eSign Genie's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.developer-api.foxit.com/
- **API base URL:** `https://na1.foxitesign.foxit.com/api`

## Authentication

### Foxit eSign OAuth2

OAuth2 client-credentials authentication for Foxit eSign API access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://na1.foxitesign.foxit.com/api/oauth2/access_token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read-write`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.developer-api.foxit.com/#authorization-foxit-esign-apis)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Envelope](actions/cancel-envelope.md) | `POST /folders/cancelFolder` | [docs](https://docs.developer-api.foxit.com/) |
| [Create Envelope from Template](actions/create-envelope-from-template.md) | `POST /templates/createFolder` | [docs](https://docs.developer-api.foxit.com/) |
| [Create Envelope from URL](actions/create-envelope-from-url.md) | `POST /folders/createfolder` | [docs](https://docs.developer-api.foxit.com/) |
| [Create Template from URL](actions/create-template-from-url.md) | `POST /templates/createtemplate` | [docs](https://docs.developer-api.foxit.com/) |
| [Create User](actions/create-user.md) | `POST /users/create` | [docs](https://docs.developer-api.foxit.com/) |
| [Create Webhook Channel](actions/create-webhook-channel.md) | `POST /webhook/createwebhookchannel` | [docs](https://docs.developer-api.foxit.com/) |
| [Deactivate Webhook Channel](actions/deactivate-webhook-channel.md) | `GET /webhook/channeldeactivate` | [docs](https://docs.developer-api.foxit.com/) |
| [Delete Envelopes](actions/delete-envelopes.md) | `POST /folders/delete` | [docs](https://docs.developer-api.foxit.com/) |
| [Delete Webhook Channel](actions/delete-webhook-channel.md) | `POST /webhook/deletechannels` | [docs](https://docs.developer-api.foxit.com/) |
| [Download Envelope Files](actions/download-envelope-files.md) | `GET /folders/download` | [docs](https://docs.developer-api.foxit.com/) |
| [Download Report](actions/download-report.md) | `POST /folders/getFolders/download` | [docs](https://docs.developer-api.foxit.com/) |
| [Download Single Document PDF](actions/download-single-document-pdf.md) | `GET /folders/document/download` | [docs](https://docs.developer-api.foxit.com/) |
| [Get a List of All Templates](actions/get-a-list-of-all-templates.md) | `GET /templates/list` | [docs](https://docs.developer-api.foxit.com/) |
| [Get Envelope Activity History](actions/get-envelope-activity-history.md) | `GET /folders/viewActivityHistory` | [docs](https://docs.developer-api.foxit.com/) |
| [Get Envelope Details](actions/get-envelope-details.md) | `GET /folders/myfolder` | [docs](https://docs.developer-api.foxit.com/) |
| [Get Envelope Ids](actions/get-envelope-ids.md) | `GET /folders/getAllFolderIdsByStatus` | [docs](https://docs.developer-api.foxit.com/) |
| [Get Template Details](actions/get-template-details.md) | `GET /templates/mytemplate` | [docs](https://docs.developer-api.foxit.com/) |
| [Get Templates by Template IDs](actions/get-templates-by-template-i-ds.md) | `POST /templates/templateDetails` | [docs](https://docs.developer-api.foxit.com/) |
| [Get Webhook Channel Details](actions/get-webhook-channel-details.md) | `GET /webhook/mychannel` | [docs](https://docs.developer-api.foxit.com/) |
| [List All Webhook Channels](actions/list-all-webhook-channels.md) | `GET /webhook/channellist` | [docs](https://docs.developer-api.foxit.com/) |
| [List All Users](actions/list-users.md) | `GET /users/list` | [docs](https://docs.developer-api.foxit.com/) |
| [Modify Shared Envelope](actions/modify-shared-envelope.md) | `POST /folders/modifySharedFolder` | [docs](https://docs.developer-api.foxit.com/) |
| [Move Envelopes to Recycle Bin](actions/move-envelopes-to-recycle-bin.md) | `POST /folders/movetorecyclebin` | [docs](https://docs.developer-api.foxit.com/) |
| [Reactivate Webhook Channel](actions/reactivate-webhook-channel.md) | `GET /webhook/channelreactivate` | [docs](https://docs.developer-api.foxit.com/) |
| [Send Draft Envelope](actions/send-draft-envelope.md) | `POST /folders/sendDraftFolder` | [docs](https://docs.developer-api.foxit.com/) |
| [Send Signature Reminder](actions/send-signature-reminder.md) | `POST /folders/signaturereminder` | [docs](https://docs.developer-api.foxit.com/) |
| [Update Envelope Fields](actions/update-envelope-fields.md) | `POST /folders/updateEnvelopeFields` | [docs](https://docs.developer-api.foxit.com/) |
| [Update Envelope Recipients](actions/update-envelope-recipients.md) | `POST /folders/updateFolder` | [docs](https://docs.developer-api.foxit.com/) |
| [Update User](actions/update-user.md) | `POST /users/update` | [docs](https://docs.developer-api.foxit.com/) |
| [Update Webhook Channel](actions/update-webhook-channel.md) | `POST /webhook/updatewebhookchannel` | [docs](https://docs.developer-api.foxit.com/) |
