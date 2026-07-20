# <img src="https://images.mindcloud.co/apps/icons/app-icon3_1777311625410.png" alt="Smsmobileapi logo" width="28" height="28"> Smsmobileapi: Universal API

SMSMobileAPI turns connected mobile phones into SMS, call, notification, and messaging gateways that you can automate through a dashboard and REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smsmobileapi/latest
- **Category:** Communication / Team Messaging
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://smsmobileapi.com/
- **Vendor API docs:** https://smsmobileapi.com/documentations-api-smsmobileapi/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Connected Mobiles](actions/list-connected-mobiles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-connected-mobiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Calls

| Action | Method | Description |
| --- | --- | --- |
| [List Missed Calls](actions/list-missed-calls.md) | GET | Retrieves missed calls from Smsmobileapi. |

### Connected Mobile

| Action | Method | Description |
| --- | --- | --- |
| [List Connected Mobiles](actions/list-connected-mobiles.md) | GET | Retrieves connected gateway mobiles from Smsmobileapi. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [List SMS Conversations](actions/list-sms-conversations.md) | GET | Retrieves SMS conversations from Smsmobileapi. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List API Sent SMS](actions/list-api-sent-sms.md) | GET | Retrieves SMS messages sent through Smsmobileapi. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from Smsmobileapi. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Set WhatsApp Retrieval Status](actions/set-whatsapp-retrieval-status.md) | PUT | Updates WhatsApp retrieval status in Smsmobileapi. |

