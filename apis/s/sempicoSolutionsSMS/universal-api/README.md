# <img src="https://images.mindcloud.co/apps/icons/sempico-icon_1778273729790.jpeg" alt="Sempico Solutions SMS logo" width="28" height="28"> Sempico Solutions SMS: Universal API

Sempico Solutions SMS provides REST API access for sending SMS messages, querying sent-message information, managing recipient groups, and maintaining personal blacklist entries for Gatum/Sempico messaging accounts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sempicoSolutionsSMS/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sempico.solutions/
- **Vendor API docs:** https://restapi.gatum.io/desc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Information](actions/get-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET |  |

### Blacklisted Number

| Action | Method | Description |
| --- | --- | --- |
| [Add Numbers to Blacklist](actions/add-numbers-to-blacklist.md) | POST |  |
| [Delete Blacklist Numbers](actions/delete-blacklist-numbers.md) | DELETE |  |

### Bulk Sms Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Send Bulk SMS](actions/send-bulk-sms.md) | POST |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST |  |
| [Delete Groups](actions/delete-groups.md) | DELETE |  |
| [List Groups](actions/list-groups.md) | GET |  |

### Group Number

| Action | Method | Description |
| --- | --- | --- |
| [Add Numbers to Group](actions/add-numbers-to-group.md) | POST |  |
| [Delete Group Numbers](actions/delete-group-numbers.md) | DELETE |  |
| [Search Group Numbers](actions/search-group-numbers.md) | GET |  |

### Sent Sms

| Action | Method | Description |
| --- | --- | --- |
| [Search Sent SMS](actions/search-sent-sms.md) | GET |  |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS](actions/send-sms.md) | POST |  |

