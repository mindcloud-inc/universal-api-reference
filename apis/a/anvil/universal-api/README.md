# <img src="https://images.mindcloud.co/apps/icons/group-1_1780947574384.png" alt="Anvil logo" width="28" height="28"> Anvil: Universal API

Anvil is a document automation platform for PDF templates, webforms, workflows, e-signature packets, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/anvil/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.useanvil.com
- **Vendor API docs:** https://www.useanvil.com/docs/api/graphql/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Cast

| Action | Method | Description |
| --- | --- | --- |
| [Create Cast](actions/create-cast.md) | POST | Creates a new cast in Anvil. |
| [Get Cast](actions/get-cast.md) | GET | Retrieves a single cast from Anvil. |
| [Publish Cast](actions/publish-cast.md) | PUT | Publishes an existing cast in Anvil. |
| [Update Cast](actions/update-cast.md) | PUT | Updates an existing cast in Anvil. |

### Document Group

| Action | Method | Description |
| --- | --- | --- |
| [Void Document Group](actions/void-document-group.md) | PUT | Voids a document group in Anvil. |

### Etch Packet

| Action | Method | Description |
| --- | --- | --- |
| [Create Etch Packet](actions/create-etch-packet.md) | POST | Creates a new Etch packet in Anvil. |
| [Generate Etch Sign URL](actions/generate-etch-sign-url.md) | GET | Generates an embedded signing URL in Anvil. |
| [Get Etch Packet](actions/get-etch-packet.md) | GET | Retrieves an Etch packet from Anvil. |
| [Remove Etch Packet](actions/remove-etch-packet.md) | DELETE | Deletes an existing Etch packet from Anvil. |
| [Send Etch Packet](actions/send-etch-packet.md) | PUT | Sends or resends an Etch packet in Anvil. |
| [Update Etch Packet](actions/update-etch-packet.md) | PUT | Updates an existing Etch packet in Anvil. |

### Forge

| Action | Method | Description |
| --- | --- | --- |
| [Create Forge](actions/create-forge.md) | POST | Creates a new forge in Anvil. |
| [Get Forge](actions/get-forge.md) | GET | Retrieves a single forge from Anvil. |
| [Update Forge](actions/update-forge.md) | PUT | Updates an existing forge in Anvil. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves a single organization from Anvil. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in Anvil. |

### Signer

| Action | Method | Description |
| --- | --- | --- |
| [Expire Signer Tokens](actions/expire-signer-tokens.md) | PUT | Expires a signer's active tokens in Anvil. |
| [Get Signer](actions/get-signer.md) | GET | Retrieves a single signer from Anvil. |
| [Notify Signer](actions/notify-signer.md) | PUT | Notifies a signer by email in Anvil. |
| [Skip Signer](actions/skip-signer.md) | PUT | Skips an existing signer in Anvil. |
| [Update Signer](actions/update-signer.md) | PUT | Updates an existing signer in Anvil. |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Create Submission](actions/create-submission.md) | POST | Creates a new submission in Anvil. |
| [Get Submission](actions/get-submission.md) | GET | Retrieves a single submission from Anvil. |
| [Submit Forge](actions/submit-forge.md) | POST | Submits data to a Forge webform in Anvil. |
| [Update Submission](actions/update-submission.md) | PUT | Updates an existing submission in Anvil. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Anvil. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Anvil. |
| [Remove Webhook](actions/remove-webhook.md) | DELETE | Deletes an existing webhook from Anvil. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Anvil. |

### Webhook Action

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Action](actions/create-webhook-action.md) | POST | Creates a new webhook action in Anvil. |
| [Remove Webhook Action](actions/remove-webhook-action.md) | DELETE | Deletes an existing webhook action from Anvil. |

### Webhook Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Log](actions/get-webhook-log.md) | GET | Retrieves a webhook log from Anvil. |

### Weld

| Action | Method | Description |
| --- | --- | --- |
| [Create Weld](actions/create-weld.md) | POST | Creates a new weld in Anvil. |
| [Get Weld](actions/get-weld.md) | GET | Retrieves a single weld from Anvil. |
| [Publish Weld](actions/publish-weld.md) | PUT | Publishes an existing weld in Anvil. |
| [Update Weld](actions/update-weld.md) | PUT | Updates an existing weld in Anvil. |

### Weld Data

| Action | Method | Description |
| --- | --- | --- |
| [Create Weld Data](actions/create-weld-data.md) | POST | Creates new weld data in Anvil. |
| [Get Weld Data](actions/get-weld-data.md) | GET | Retrieves a single weld data record from Anvil. |
| [Remove Weld Data](actions/remove-weld-data.md) | DELETE | Deletes existing weld data from Anvil. |
| [Update Weld Data](actions/update-weld-data.md) | PUT | Updates existing weld data in Anvil. |

