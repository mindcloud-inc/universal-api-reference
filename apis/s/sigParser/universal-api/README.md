# <img src="https://images.mindcloud.co/apps/icons/sig-parser_1775842595862.png" alt="SigParser logo" width="28" height="28"> SigParser: Universal API

Extract contacts, companies, and relationship data from email activity

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sigParser/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sigparser.com
- **Vendor API docs:** https://ipaas.sigparser.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Revoke Current API Key](actions/revoke-current-api-key.md) | DELETE |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company By Domain](actions/get-company-by-domain.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |
| [List Updated Companies](actions/list-updated-companies.md) | GET |  |

### Company Interaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact-to-Company Interaction Graph](actions/get-contact-to-company-interaction-graph.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact By Email](actions/get-contact-by-email.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [List Contacts By Company Domain](actions/list-contacts-by-company-domain.md) | GET |  |
| [List Contacts With Relationship Metrics](actions/list-contacts-with-relationship-metrics.md) | GET |  |
| [List Updated Contacts](actions/list-updated-contacts.md) | GET |  |
| [Parse Signature From JSON](actions/parse-signature-from-json.md) | GET |  |
| [Parse Signature From MIME/EML](actions/parse-signature-from-mime-eml.md) | GET |  |
| [Parse Signature From MSG](actions/parse-signature-from-msg.md) | GET |  |
| [Upsert Contact](actions/upsert-contact.md) | POST |  |

### Contact Interaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact-to-Contact Interaction Graph](actions/get-contact-to-contact-interaction-graph.md) | GET |  |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Get Email By Message ID](actions/get-email-by-message-id.md) | GET |  |
| [List Distinct Emails](actions/list-distinct-emails.md) | GET |  |
| [List Emails By Contact](actions/list-emails-by-contact.md) | GET |  |
| [List Newly Ingested Emails](actions/list-newly-ingested-emails.md) | GET |  |
| [Split Email From MIME/EML](actions/split-email-from-mime-eml.md) | GET |  |
| [Split Email From MSG](actions/split-email-from-msg.md) | GET |  |

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [Get Meeting By ICalUID](actions/get-meeting-by-i-cal-uid.md) | GET |  |
| [List Distinct Meetings](actions/list-distinct-meetings.md) | GET |  |
| [List Meetings By Attendee Email](actions/list-meetings-by-attendee-email.md) | GET |  |
| [List Updated Meetings](actions/list-updated-meetings.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook By ID](actions/get-webhook-by-id.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

