# <img src="https://images.mindcloud.co/apps/icons/crexendo_1774984619190.png" alt="Crexendo logo" width="28" height="28"> Crexendo: Universal API

Crexendo provides NS API-powered cloud communications and contact-center operations for domains, users, devices, calling, contacts, messaging, meetings, and numbering.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/crexendo/latest
- **Category:** Support / Contact Center
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.crexendo.com
- **Vendor API docs:** https://docs.ns-api.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Domains](actions/list-domains.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-domains?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [List Domain Addresses](actions/list-domain-addresses.md) | GET | Retrieves addresses for a domain in Crexendo. |
| [List User Addresses](actions/list-user-addresses.md) | GET | Retrieves addresses for a user in Crexendo. |

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [List Domain Agents](actions/list-domain-agents.md) | GET | Retrieves agents for a domain in Crexendo. |

### Answer Rule

| Action | Method | Description |
| --- | --- | --- |
| [List My Answer Rules](actions/list-my-answer-rules.md) | GET | Retrieves your answer rules from Crexendo. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Get API Key Info](actions/get-api-key-info.md) | GET | Retrieves API key info from Crexendo. |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Count Domain Active Calls](actions/count-domain-active-calls.md) | GET | Retrieves an active call count for a domain in Crexendo. |
| [List Domain Active Calls](actions/list-domain-active-calls.md) | GET | Retrieves active calls for a domain in Crexendo. |
| [List User Active Calls](actions/list-user-active-calls.md) | GET | Retrieves active calls for a user in Crexendo. |

### Call Queue

| Action | Method | Description |
| --- | --- | --- |
| [List Call Queues](actions/list-call-queues.md) | GET | Retrieves call queues for a domain in Crexendo. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Count User Contacts](actions/count-user-contacts.md) | GET | Retrieves a contact count for a user in Crexendo. |
| [List Domain Contacts](actions/list-domain-contacts.md) | GET | Retrieves contacts for a domain in Crexendo. |
| [List My Contacts](actions/list-my-contacts.md) | GET | Retrieves your contacts from Crexendo. |
| [List User Contacts](actions/list-user-contacts.md) | GET | Retrieves contacts for a user in Crexendo. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List User Devices](actions/list-user-devices.md) | GET | Retrieves devices for a user in Crexendo. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Check Domain Exists](actions/check-domain-exists.md) | GET | Checks whether a domain exists in Crexendo. |
| [Count Domains](actions/count-domains.md) | GET | Retrieves a domain count from Crexendo. |
| [Get Domain](actions/get-domain.md) | GET | Retrieves a domain from Crexendo. |
| [Get Domain Billing Summary](actions/get-domain-billing-summary.md) | GET | Retrieves a domain billing summary from Crexendo. |
| [Get My Domain Info](actions/get-my-domain-info.md) | GET | Retrieves your domain info from Crexendo. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from Crexendo. |

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [List User Meetings](actions/list-user-meetings.md) | GET | Retrieves meetings for a user in Crexendo. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [List Domain Phone Numbers](actions/list-domain-phone-numbers.md) | GET | Retrieves phone numbers for a domain in Crexendo. |
| [List Phone Numbers](actions/list-phone-numbers.md) | GET | Retrieves phone numbers from Crexendo. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [List Sites](actions/list-sites.md) | GET | Retrieves sites for a domain in Crexendo. |

### Sms Number

| Action | Method | Description |
| --- | --- | --- |
| [List Domain SMS Numbers](actions/list-domain-sms-numbers.md) | GET | Retrieves SMS numbers for a domain in Crexendo. |
| [List User SMS Numbers](actions/list-user-sms-numbers.md) | GET | Retrieves SMS numbers for a user in Crexendo. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Count Users](actions/count-users.md) | GET | Retrieves a user count for a domain in Crexendo. |
| [Get My User](actions/get-my-user.md) | GET | Retrieves your user info from Crexendo. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Crexendo. |
| [List Users](actions/list-users.md) | GET | Retrieves users for a domain in Crexendo. |

