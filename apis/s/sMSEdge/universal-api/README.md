# <img src="https://images.mindcloud.co/apps/icons/favicon_1777311195511.png" alt="SMSEdge logo" width="28" height="28"> SMSEdge: Universal API

Send SMS campaigns, manage contacts, and track delivery performance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMSEdge/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://smsedge.com
- **Vendor API docs:** https://developers.smsedge.io/reference/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Details](actions/get-user-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Automation

| Action | Method | Description |
| --- | --- | --- |
| [Get Automations](actions/get-automations.md) | GET | Retrieves automation records and details from SMSEdge. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaigns](actions/get-campaigns.md) | GET | Retrieves campaign records and details from SMSEdge. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in a SMSEdge list. |
| [Delete Contacts](actions/delete-contacts.md) | DELETE | Deletes contacts from a SMSEdge list. |
| [Get Contacts](actions/get-contacts.md) | GET | Retrieves contact records and details from SMSEdge. |
| [Get Unsubscribed Numbers](actions/get-unsubscribed-numbers.md) | GET | Retrieves unsubscribed phone numbers from SMSEdge. |
| [Resubscribe Number](actions/resubscribe-number.md) | DELETE | Resubscribes a phone number in SMSEdge. |
| [Unsubscribe Number](actions/unsubscribe-number.md) | POST | Unsubscribes a phone number in SMSEdge. |
| [Verify Number Format](actions/verify-number-format.md) | GET | Verifies phone number format in SMSEdge. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [Get Countries](actions/get-countries.md) | GET | Retrieves country reference data from SMSEdge. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in SMSEdge. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing list from SMSEdge. |
| [Get List Details](actions/get-list-details.md) | GET | Retrieves details for a list in SMSEdge. |
| [Get Lists](actions/get-lists.md) | GET | Retrieves lists and their details from SMSEdge. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Analyze SMS Text](actions/analyze-sms-text.md) | GET | Analyzes SMS text before sending in SMSEdge. |
| [Get SMS Message Details](actions/get-sms-message-details.md) | GET | Retrieves sent SMS details from SMSEdge. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Sending Reports](actions/get-sending-reports.md) | GET | Retrieves SMS sending reports from SMSEdge. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [Get Routes](actions/get-routes.md) | GET | Retrieves available routing options from SMSEdge. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get HTTP Status Codes](actions/get-http-status-codes.md) | GET | Retrieves HTTP status codes from SMSEdge. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves API user details from SMSEdge. |

