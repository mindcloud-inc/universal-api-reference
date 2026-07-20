# <img src="https://images.mindcloud.co/apps/icons/emailchef_1774543689373.png" alt="Emailchef logo" width="28" height="28"> Emailchef: Universal API

Emailchef is an email marketing platform for managing lists, contacts, segments, campaigns, imports, and transactional sends.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emailchef/latest
- **Category:** Marketing
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://emailchef.com/
- **Vendor API docs:** https://emailchef.com/integration/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/list-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Clone Campaign](actions/clone-campaign.md) | POST | Creates a cloned campaign in Emailchef. |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Emailchef. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from Emailchef. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Emailchef. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves all campaigns from Emailchef. |
| [Schedule Campaign](actions/schedule-campaign.md) | PUT | Schedules a campaign in Emailchef. |
| [Send Campaign](actions/send-campaign.md) | PUT | Sends a campaign in Emailchef. |
| [Send Test Campaign](actions/send-test-campaign.md) | PUT | Sends a test campaign email in Emailchef. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Emailchef. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Emailchef. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Emailchef. |
| [Import Contacts](actions/import-contacts.md) | POST | Imports contacts into an Emailchef list. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Emailchef. |
| [Unsubscribe Contact From List](actions/unsubscribe-contact-from-list.md) | PUT | Unsubscribes a contact from an Emailchef list. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Emailchef. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new mailing list in Emailchef. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing mailing list from Emailchef. |
| [Get List](actions/get-list.md) | GET | Retrieves a mailing list from Emailchef. |
| [Get List Stats](actions/get-list-stats.md) | GET | Retrieves mailing list statistics from Emailchef. |
| [List Lists](actions/list-lists.md) | GET | Retrieves all mailing lists from Emailchef. |
| [Update List](actions/update-list.md) | PUT | Updates an existing mailing list in Emailchef. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a new segment in Emailchef. |
| [Get Segment](actions/get-segment.md) | GET | Retrieves a segment from Emailchef. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments for a list from Emailchef. |
| [Update Segment](actions/update-segment.md) | PUT | Updates an existing segment in Emailchef. |

