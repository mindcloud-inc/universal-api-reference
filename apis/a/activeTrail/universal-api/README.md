# <img src="https://images.mindcloud.co/apps/icons/active-trail_1773848702049.png" alt="ActiveTrail logo" width="28" height="28"> ActiveTrail: Universal API

Manage contacts, groups, campaigns, and messages in ActiveTrail

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/activeTrail/latest
- **Category:** Marketing
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.activetrail.com
- **Vendor API docs:** https://webapi.mymarketing.co.il/api/docs/Guides

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Campaigns](actions/list-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET | Retrieves account email and SMS balances from ActiveTrail. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from ActiveTrail. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves a list of campaigns from ActiveTrail. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in ActiveTrail. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in ActiveTrail. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from ActiveTrail. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from ActiveTrail. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from ActiveTrail. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in ActiveTrail. |

### Contact Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Contacts](actions/import-contacts.md) | POST | Imports contacts into a group in ActiveTrail. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in ActiveTrail. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from ActiveTrail. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from ActiveTrail. |
| [List Groups](actions/list-groups.md) | GET | Retrieves a list of groups from ActiveTrail. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in ActiveTrail. |

### Group Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact to Group](actions/add-contact-to-group.md) | POST | Adds a contact to a group in ActiveTrail. |
| [List Group Members](actions/list-group-members.md) | GET | Retrieves members of a group from ActiveTrail. |
| [Remove Member from Group](actions/remove-member-from-group.md) | DELETE | Removes a member from a group in ActiveTrail. |

### Mailing List

| Action | Method | Description |
| --- | --- | --- |
| [Create Mailing List](actions/create-mailing-list.md) | POST | Creates a new mailing list in ActiveTrail. |
| [Delete Mailing List](actions/delete-mailing-list.md) | DELETE | Deletes an existing mailing list from ActiveTrail. |
| [Get Mailing List](actions/get-mailing-list.md) | GET | Retrieves a mailing list from ActiveTrail. |
| [List Mailing Lists](actions/list-mailing-lists.md) | GET | Retrieves mailing lists from ActiveTrail. |

### Operational Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Email Operational Message to Contacts](actions/send-email-operational-message-to-contacts.md) | POST | Sends an operational email to contacts in ActiveTrail. |

