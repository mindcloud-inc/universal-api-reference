# <img src="https://images.mindcloud.co/apps/icons/joonto_1775138824176.png" alt="Joonto logo" width="28" height="28"> Joonto: Universal API

Mobile phone cloud platform for your business.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/joonto/latest
- **Category:** Support / Contact Center
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://joonto.com
- **Vendor API docs:** https://api.joonto.com/docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List SMS Contacts](actions/list-sms-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joonto/latest/actions/list-sms-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Details](actions/get-call-details.md) | GET |  |
| [Get Calls Leaderboard](actions/get-calls-leaderboard.md) | GET |  |
| [Get Dashboard Call Summary](actions/get-dashboard-call-summary.md) | GET |  |
| [List Live Calls](actions/list-live-calls.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Avatar Image By Contact](actions/get-avatar-image-by-contact.md) | GET |  |
| [List SMS Contacts](actions/list-sms-contacts.md) | GET |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS By User And Phone Number](actions/get-sms-by-user-and-phone-number.md) | GET |  |
| [Get SMS Details](actions/get-sms-details.md) | GET |  |
| [List New SMS By User](actions/list-new-sms-by-user.md) | GET |  |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Get Caller Name](actions/get-caller-name.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET |  |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Avatar Image By User Email](actions/get-avatar-image-by-user-email.md) | GET |  |
| [Get Current User](actions/get-current-user.md) | GET |  |

