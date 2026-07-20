# <img src="https://images.mindcloud.co/apps/icons/images-3_1773690651598.png" alt="Moosend logo" width="28" height="28"> Moosend: Universal API

Manage email lists, subscribers, segments, and campaigns

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moosend/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://moosend.com/
- **Vendor API docs:** https://docs.moosend.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Active Mailing Lists](actions/list-active-mailing-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-active-mailing-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Campaign](actions/create-draft-campaign.md) | POST | Creates a draft campaign in Moosend. |
| [Get Campaign Details](actions/get-campaign-details.md) | GET | Retrieves campaign details from Moosend. |
| [Get Campaign Link Activity](actions/get-campaign-link-activity.md) | GET | Retrieves campaign link activity from Moosend. |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | GET | Retrieves campaign statistics from Moosend. |
| [Get Campaign Summary](actions/get-campaign-summary.md) | GET | Retrieves campaign summary from Moosend. |
| [List Campaigns By Page And Page Size](actions/list-campaigns-by-page-and-page-size.md) | GET | Retrieves campaigns from Moosend by page and page size. |
| [Schedule Campaign](actions/schedule-campaign.md) | PUT | Schedules a campaign in Moosend. |
| [Send Campaign](actions/send-campaign.md) | PUT | Sends a campaign in Moosend. |
| [Test Campaign](actions/test-campaign.md) | PUT | Tests a campaign in Moosend. |
| [Unschedule Campaign](actions/unschedule-campaign.md) | PUT | Unschedules a campaign in Moosend. |
| [Update Draft Campaign](actions/update-draft-campaign.md) | PUT | Updates a draft campaign in Moosend. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in Moosend. |
| [Remove Custom Field](actions/remove-custom-field.md) | DELETE | Deletes an existing custom field from Moosend. |
| [Update Custom Field](actions/update-custom-field.md) | PUT | Updates an existing custom field in Moosend. |

### Mailing List

| Action | Method | Description |
| --- | --- | --- |
| [Create Mailing List](actions/create-mailing-list.md) | POST | Creates a new mailing list in Moosend. |
| [Delete Mailing List](actions/delete-mailing-list.md) | DELETE | Deletes an existing mailing list from Moosend. |
| [Get Mailing List Details](actions/get-mailing-list-details.md) | GET | Retrieves mailing list details from Moosend. |
| [List Active Mailing Lists](actions/list-active-mailing-lists.md) | GET | Retrieves active mailing lists from Moosend. |
| [List Active Mailing Lists With Paging](actions/list-active-mailing-lists-with-paging.md) | GET | Retrieves active mailing lists from Moosend with paging. |
| [Update Mailing List](actions/update-mailing-list.md) | PUT | Updates an existing mailing list in Moosend. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a new empty segment in Moosend. |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes an existing segment from Moosend. |
| [Get Segment Details](actions/get-segment-details.md) | GET | Retrieves segment details from Moosend. |
| [List Segment Subscribers](actions/list-segment-subscribers.md) | GET | Retrieves segment subscribers from Moosend. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from Moosend. |
| [Update Segment](actions/update-segment.md) | PUT | Updates an existing segment in Moosend. |

### Segment Criteria

| Action | Method | Description |
| --- | --- | --- |
| [Add Segment Criteria](actions/add-segment-criteria.md) | PUT | Adds criteria to a segment in Moosend. |
| [Update Segment Criteria](actions/update-segment-criteria.md) | PUT | Updates segment criteria in Moosend. |

### Sender

| Action | Method | Description |
| --- | --- | --- |
| [List Senders](actions/list-senders.md) | GET | Retrieves senders from Moosend. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add Multiple Subscribers](actions/add-multiple-subscribers.md) | POST | Creates multiple subscribers in Moosend. |
| [Add New Subscriber](actions/add-new-subscriber.md) | POST | Creates a new subscriber in Moosend. |
| [Get Subscriber By Email Address](actions/get-subscriber-by-email-address.md) | GET | Finds a subscriber in Moosend by email address. |
| [Get Subscriber By Id](actions/get-subscriber-by-id.md) | GET | Retrieves a subscriber from Moosend by ID. |
| [Get Subscriber By Id Without Mailing List Id](actions/get-subscriber-by-id-without-mailing-list-id.md) | GET | Retrieves a subscriber from Moosend by ID only. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from Moosend by status. |
| [Remove Multiple Subscribers](actions/remove-multiple-subscribers.md) | DELETE | Deletes multiple subscribers from Moosend. |
| [Remove Subscriber](actions/remove-subscriber.md) | DELETE | Deletes an existing subscriber from Moosend. |
| [Unsubscribe Subscriber From Account](actions/unsubscribe-subscriber-from-account.md) | PUT | Unsubscribes a subscriber from a Moosend account. |
| [Unsubscribe Subscriber From Mailing List](actions/unsubscribe-subscriber-from-mailing-list.md) | PUT | Unsubscribes a subscriber from a Moosend mailing list. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in Moosend. |

