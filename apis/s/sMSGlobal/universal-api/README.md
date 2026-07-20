# <img src="https://images.mindcloud.co/apps/icons/id4zyx29d1-logos_1774631163485.png" alt="SMSGlobal logo" width="28" height="28"> SMSGlobal: Universal API

Send SMSGlobal messages and manage contacts, groups, and account settings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMSGlobal/latest
- **Category:** Communication / Team Messaging
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smsglobal.com
- **Vendor API docs:** https://www.smsglobal.com/rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Contact Details](actions/get-user-contact-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/get-user-contact-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Auto Top-up

| Action | Method | Description |
| --- | --- | --- |
| [Get Auto Top-up](actions/get-auto-top-up.md) | GET | Retrieves auto top-up settings for the SMSGlobal account. |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves the SMSGlobal account credit balance. |
| [Get Low Balance Alerts](actions/get-low-balance-alerts.md) | GET | Retrieves low balance alert settings for the SMSGlobal account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from SMSGlobal by ID. |
| [List Group Contacts](actions/list-group-contacts.md) | GET | Retrieves contacts from an SMSGlobal contact group. |

### Dedicated Number

| Action | Method | Description |
| --- | --- | --- |
| [List Dedicated Numbers](actions/list-dedicated-numbers.md) | GET | Retrieves dedicated numbers from the SMSGlobal account. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a contact group from SMSGlobal by ID. |
| [List Groups](actions/list-groups.md) | GET | Retrieves contact groups from the SMSGlobal account. |

### Incoming Message

| Action | Method | Description |
| --- | --- | --- |
| [List Incoming Messages](actions/list-incoming-messages.md) | GET | Retrieves incoming messages from the SMSGlobal account. |

### Number

| Action | Method | Description |
| --- | --- | --- |
| [List Pending Verified Numbers](actions/list-pending-verified-numbers.md) | GET | Retrieves pending verified numbers from the SMSGlobal account. |
| [List Verified Numbers](actions/list-verified-numbers.md) | GET | Retrieves verified numbers from the SMSGlobal account. |

### Optout

| Action | Method | Description |
| --- | --- | --- |
| [List Opt-Outs](actions/list-opt-outs.md) | GET | Retrieves opted-out numbers from the SMSGlobal account. |

### Outgoing Message

| Action | Method | Description |
| --- | --- | --- |
| [List Outgoing Messages](actions/list-outgoing-messages.md) | GET | Retrieves outgoing messages from the SMSGlobal account. |

### Pools

| Action | Method | Description |
| --- | --- | --- |
| [List Shared Pools](actions/list-shared-pools.md) | GET | Retrieves shared pools from the SMSGlobal account. |

### Sender Id

| Action | Method | Description |
| --- | --- | --- |
| [List Sender IDs](actions/list-sender-ids.md) | GET | Retrieves sender IDs from the SMSGlobal account. |

### User Billing Details

| Action | Method | Description |
| --- | --- | --- |
| [Get User Billing Details](actions/get-user-billing-details.md) | GET | Retrieves billing details for the authenticated SMSGlobal account. |

### User Contact Details

| Action | Method | Description |
| --- | --- | --- |
| [Get User Contact Details](actions/get-user-contact-details.md) | GET | Retrieves contact details for the authenticated SMSGlobal account. |

