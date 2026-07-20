# Sign: Native API Reference

A consolidated summary of Sign's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://developers.cm.com/sign/docs/introduction
- **API base URL:** `https://api.cm.com/sign-sandbox/v1`

## Authentication

### Sign API credentials

Connect CM.com Sign using a Key ID and Key Secret. The app generates the required HS256 bearer token for each request.

### Credentials

- **Key ID:** `keyId` · required · CM.com Sign Key ID used as the JWT header kid value.
- **Key Secret:** `keySecret` · required · CM.com Sign Key Secret used to sign the HS256 bearer token.

[Official authentication documentation](https://developers.cm.com/sign/docs/getting-started)

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add webhook](actions/add-webhook.md) | `POST /clients/{kid}/webhooks` | [docs](https://developers.cm.com/sign/reference/post_clients-kid-webhooks) |
| [Create dossier](actions/create-dossier.md) | `POST /dossiers` | [docs](https://developers.cm.com/sign/reference/post_dossiers) |
| [Create invites](actions/create-invites.md) | `POST /dossiers/{dossierId}/invites` | [docs](https://developers.cm.com/sign/reference/post_dossiers-dossierid-invites) |
| [Create template](actions/create-template.md) | `POST /templates` | [docs](https://developers.cm.com/sign/reference/post_templates) |
| [Delete template](actions/delete-template.md) | `DELETE /templates/{id}` | [docs](https://developers.cm.com/sign/reference/delete_templates-id) |
| [Delete webhook](actions/delete-webhook.md) | `DELETE /clients/{kid}/webhooks/{webhookId}` | [docs](https://developers.cm.com/sign/reference/delete_clients-kid-webhooks-webhookid) |
| [Get all templates](actions/get-all-templates.md) | `GET /templates` | [docs](https://developers.cm.com/sign/reference/get_templates) |
| [Get dossier](actions/get-dossier.md) | `GET /dossiers/{dossierId}` | [docs](https://developers.cm.com/sign/reference/get_dossiers-dossierid) |
| [Get invite](actions/get-invite.md) | `GET /dossiers/{dossierId}/invites/{inviteId}` | [docs](https://developers.cm.com/sign/reference/get_dossiers-dossierid-invites-inviteid) |
| [Get template](actions/get-template.md) | `GET /templates/{id}` | [docs](https://developers.cm.com/sign/reference/get_templates-id) |
| [Get webhook](actions/get-webhook.md) | `GET /clients/{kid}/webhooks/{webhookId}` | [docs](https://developers.cm.com/sign/reference/get_clients-kid-webhooks-webhookid) |
| [List clients](actions/list-clients.md) | `GET /clients` | [docs](https://developers.cm.com/sign/reference/get_clients) |
| [Seal a document](actions/seal-a-document.md) | `POST /seal` | [docs](https://developers.cm.com/sign/reference/post_seal) |
| [Update invitee](actions/update-invitee.md) | `PUT /dossiers/{dossierId}/invitees/{inviteeId}` | [docs](https://developers.cm.com/sign/reference/put_dossiers-dossierid-invitees-inviteeid) |
| [Update template](actions/update-template.md) | `PUT /templates/{id}` | [docs](https://developers.cm.com/sign/reference/put_templates-id) |
| [Update webhook](actions/update-webhook.md) | `PUT /clients/{kid}/webhooks/{webhookId}` | [docs](https://developers.cm.com/sign/reference/put_clients-kid-webhooks-webhookid) |
| [Upload document](actions/upload-document.md) | `POST /upload` | [docs](https://developers.cm.com/sign/reference/post_upload) |
