# <img src="https://images.mindcloud.co/apps/icons/sign-icon_1782394474874.svg" alt="Sign logo" width="28" height="28"> Sign: Universal API

Build electronic-signature dossiers, invite signers, manage clients and templates, and retrieve signed documents with CM.com Sign.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cm.com/sign/
- **Vendor API docs:** https://developers.cm.com/sign/docs/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get all templates](actions/get-all-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sign/latest/actions/get-all-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List clients](actions/list-clients.md) | GET | Retrieves available clients from CM.com Sign. |
| [Update invitee](actions/update-invitee.md) | PUT | Updates a dossier invitee in CM.com Sign. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create dossier](actions/create-dossier.md) | POST | Creates a dossier in CM.com Sign. |
| [Get dossier](actions/get-dossier.md) | GET | Retrieves a dossier from CM.com Sign by ID. |
| [Seal a document](actions/seal-a-document.md) | POST | Creates a sealed document in CM.com Sign. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Upload document](actions/upload-document.md) | POST | Uploads a document to CM.com Sign. |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [Create invites](actions/create-invites.md) | POST | Creates signing invites for a dossier in CM.com Sign. |
| [Get invite](actions/get-invite.md) | GET | Retrieves a dossier invite from CM.com Sign. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create template](actions/create-template.md) | POST | Creates a template in CM.com Sign. |
| [Delete template](actions/delete-template.md) | DELETE | Deletes a template from CM.com Sign. |
| [Get all templates](actions/get-all-templates.md) | GET | Retrieves templates from CM.com Sign. |
| [Get template](actions/get-template.md) | GET | Retrieves a template from CM.com Sign by ID. |
| [Update template](actions/update-template.md) | PUT | Updates a template in CM.com Sign. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Add webhook](actions/add-webhook.md) | POST | Creates a webhook in CM.com Sign. |
| [Delete webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from CM.com Sign. |
| [Get webhook](actions/get-webhook.md) | GET | Retrieves a webhook from CM.com Sign by ID. |
| [Update webhook](actions/update-webhook.md) | PUT | Updates a webhook in CM.com Sign. |

