# <img src="https://images.mindcloud.co/apps/icons/yaycom_1774457492440.png" alt="Yay.com logo" width="28" height="28"> Yay.com: Universal API

Manage Yay VoIP accounts, users, and phone numbers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yaycom/latest
- **Category:** Support / Contact Center
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.yay.com/
- **Vendor API docs:** https://www.yay.com/voip/api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Balance](actions/get-account-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET | Retrieves the account balance from Yay.com. |

### Call Flow

| Action | Method | Description |
| --- | --- | --- |
| [List Call Flows](actions/list-call-flows.md) | GET | Retrieves call flows from Yay.com. |

### Call Flow Extension

| Action | Method | Description |
| --- | --- | --- |
| [Get Next Call Flow Extension](actions/get-next-call-flow-extension.md) | GET | Retrieves the next call flow extension from Yay.com. |

### Call Pack

| Action | Method | Description |
| --- | --- | --- |
| [List Call Packs](actions/list-call-packs.md) | GET | Retrieves call packs from Yay.com. |

### Call Recording Retention

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Recording Retention](actions/get-call-recording-retention.md) | GET | Retrieves call recording retention from Yay.com. |

### Call Restriction Pattern

| Action | Method | Description |
| --- | --- | --- |
| [List Call Restriction Patterns](actions/list-call-restriction-patterns.md) | GET | Retrieves call restriction patterns from Yay.com. |

### Call Statistics Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Call Statistics Schedules](actions/list-call-statistics-schedules.md) | GET | Retrieves call statistics schedules from Yay.com. |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET | Retrieves departments from Yay.com. |

### Emergency Address

| Action | Method | Description |
| --- | --- | --- |
| [List Emergency Addresses](actions/list-emergency-addresses.md) | GET | Retrieves emergency addresses from Yay.com. |

### Hunt Group

| Action | Method | Description |
| --- | --- | --- |
| [List Hunt Groups](actions/list-hunt-groups.md) | GET | Retrieves hunt groups from Yay.com. |

### Hunt Group Extension

| Action | Method | Description |
| --- | --- | --- |
| [Get Next Hunt Group Extension](actions/get-next-hunt-group-extension.md) | GET | Retrieves the next hunt group extension from Yay.com. |

### International Call Restriction Exception

| Action | Method | Description |
| --- | --- | --- |
| [List Allowed International Call Exceptions](actions/list-allowed-international-call-exceptions.md) | GET | Retrieves allowed international call exceptions from Yay.com. |

### Maximum Call Cost Restriction

| Action | Method | Description |
| --- | --- | --- |
| [Get Maximum Call Cost Restriction](actions/get-maximum-call-cost-restriction.md) | GET | Retrieves the maximum call cost restriction from Yay.com. |

### Message Flow

| Action | Method | Description |
| --- | --- | --- |
| [List Message Flows](actions/list-message-flows.md) | GET | Retrieves message flows from Yay.com. |

### Missed Call Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Missed Call Notifications](actions/list-missed-call-notifications.md) | GET | Retrieves missed call notifications from Yay.com. |

### Number Address

| Action | Method | Description |
| --- | --- | --- |
| [List Number Addresses](actions/list-number-addresses.md) | GET | Retrieves number addresses from Yay.com. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Next Mailbox Menu Extension](actions/get-next-mailbox-menu-extension.md) | GET | Retrieves the next mailbox menu extension from Yay.com. |
| [List Caller ID Requests](actions/list-caller-id-requests.md) | GET | Retrieves caller ID requests from Yay.com. |
| [List Caller IDs](actions/list-caller-ids.md) | GET | Retrieves caller IDs from Yay.com. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Yay.com. |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integrations from Yay.com. |
| [List Mailbox Menus](actions/list-mailbox-menus.md) | GET | Retrieves mailbox menus from Yay.com. |
| [List Mailboxes](actions/list-mailboxes.md) | GET | Retrieves mailboxes from Yay.com. |
| [List Phone Books](actions/list-phone-books.md) | GET | Retrieves phone books from Yay.com. |
| [List Playlists](actions/list-playlists.md) | GET | Retrieves playlists from Yay.com. |
| [List Provisioning Devices](actions/list-provisioning-devices.md) | GET | Retrieves provisioning devices from Yay.com. |
| [List Short Codes](actions/list-short-codes.md) | GET | Retrieves short codes from Yay.com. |
| [List Sounds](actions/list-sounds.md) | GET | Retrieves sounds from Yay.com. |
| [List Speed Dials](actions/list-speed-dials.md) | GET | Retrieves speed dials from Yay.com. |
| [List Storefronts](actions/list-storefronts.md) | GET | Retrieves storefronts from Yay.com. |
| [List VoIP Trunks](actions/list-voip-trunks.md) | GET | Retrieves VoIP trunks from Yay.com. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [List Phone Numbers](actions/list-phone-numbers.md) | GET | Retrieves phone numbers from Yay.com. |

### Reseller Address

| Action | Method | Description |
| --- | --- | --- |
| [List Reseller Addresses](actions/list-reseller-addresses.md) | GET | Retrieves reseller addresses from Yay.com. |

### Reseller User

| Action | Method | Description |
| --- | --- | --- |
| [List Reseller Users](actions/list-reseller-users.md) | GET | Retrieves reseller users from Yay.com. |

### Sip User

| Action | Method | Description |
| --- | --- | --- |
| [List SIP Users](actions/list-sip-users.md) | GET | Retrieves SIP users from Yay.com. |

### Sip User Extension

| Action | Method | Description |
| --- | --- | --- |
| [Get Next SIP User Extension](actions/get-next-sip-user-extension.md) | GET | Retrieves the next SIP user extension from Yay.com. |

### Sip User Status

| Action | Method | Description |
| --- | --- | --- |
| [List SIP User Statuses](actions/list-sip-user-statuses.md) | GET | Retrieves SIP user statuses from Yay.com. |

### Sub Reseller

| Action | Method | Description |
| --- | --- | --- |
| [List Sub Resellers](actions/list-sub-resellers.md) | GET | Retrieves sub resellers from Yay.com. |

### Time Diary

| Action | Method | Description |
| --- | --- | --- |
| [List Time Diaries](actions/list-time-diaries.md) | GET | Retrieves time diaries from Yay.com. |

