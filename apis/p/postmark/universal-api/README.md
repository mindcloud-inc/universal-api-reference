# <img src="https://images.mindcloud.co/apps/icons/postmark_1774898404011.png" alt="Postmark logo" width="28" height="28"> Postmark: Universal API

Send, track, and manage transactional emails

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/postmark/latest
- **Category:** Communication / Email Communications
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://postmarkapp.com
- **Vendor API docs:** https://postmarkapp.com/developer/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Bounce

| Action | Method | Description |
| --- | --- | --- |
| [Get Bounce](actions/get-bounce.md) | GET | Retrieves a bounce from Postmark. |
| [List Bounces](actions/list-bounces.md) | GET | Retrieves bounces from Postmark. |
| [Reactivate Bounce](actions/reactivate-bounce.md) | PUT | Reactivates a bounce in Postmark. |

### Delivery Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Delivery Stats](actions/get-delivery-stats.md) | GET | Retrieves delivery stats from Postmark. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | POST | Creates a domain in Postmark. |
| [Get Domain](actions/get-domain.md) | GET | Retrieves a domain from Postmark. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from Postmark. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Batch Emails](actions/send-batch-emails.md) | POST | Sends batch emails through Postmark. |
| [Send Batch Template Emails](actions/send-batch-template-emails.md) | POST | Sends batch template emails through Postmark. |
| [Send Email](actions/send-email.md) | POST | Sends an email through Postmark. |
| [Send Template Email](actions/send-template-email.md) | POST | Sends a template email through Postmark. |

### Outbound Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Outbound Message Details](actions/get-outbound-message-details.md) | GET | Retrieves outbound message details from Postmark. |
| [Search Outbound Messages](actions/search-outbound-messages.md) | GET | Searches outbound messages in Postmark. |

### Outbound Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Outbound Stats Overview](actions/get-outbound-stats-overview.md) | GET | Retrieves outbound stats overview from Postmark. |

### Sender Signature

| Action | Method | Description |
| --- | --- | --- |
| [Create Sender Signature](actions/create-sender-signature.md) | POST | Creates a sender signature in Postmark. |
| [Get Sender Signature](actions/get-sender-signature.md) | GET | Retrieves a sender signature from Postmark. |
| [List Sender Signatures](actions/list-sender-signatures.md) | GET | Retrieves sender signatures from Postmark. |
| [Update Sender Signature](actions/update-sender-signature.md) | PUT | Updates a sender signature in Postmark. |

### Server

| Action | Method | Description |
| --- | --- | --- |
| [Create Server](actions/create-server.md) | POST | Creates a server in Postmark. |
| [Get Server](actions/get-server.md) | GET | Retrieves a server from Postmark. |
| [Get Server Configuration](actions/get-server-configuration.md) | GET | Retrieves the current Postmark server configuration. |
| [List Servers](actions/list-servers.md) | GET | Retrieves servers from Postmark. |
| [Update Server](actions/update-server.md) | PUT | Updates a server in Postmark. |
| [Update Server Configuration](actions/update-server-configuration.md) | PUT | Updates the current Postmark server configuration. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a template in Postmark. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes a template from Postmark. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Postmark. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Postmark. |
| [Update Template](actions/update-template.md) | PUT | Updates a template in Postmark. |
| [Validate Template](actions/validate-template.md) | POST | Validates a template in Postmark. |

