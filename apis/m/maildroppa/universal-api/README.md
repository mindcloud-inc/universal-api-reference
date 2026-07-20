# <img src="https://images.mindcloud.co/apps/icons/maildroppa-icon_1775765112663.png" alt="Maildroppa logo" width="28" height="28"> Maildroppa: Universal API

Official Maildroppa API (Beta) wrapper for subscribers, segments, tags, field types, and signup forms.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/maildroppa/latest
- **Category:** Marketing
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://maildroppa.com
- **Vendor API docs:** https://api.maildroppa.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Count Subscribers](actions/count-subscribers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/count-subscribers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Field Matcher

| Action | Method | Description |
| --- | --- | --- |
| [List Field Matchers](actions/list-field-matchers.md) | GET |  |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST |  |
| [Delete Segment](actions/delete-segment.md) | DELETE |  |
| [Get Segment](actions/get-segment.md) | GET |  |
| [List Segments](actions/list-segments.md) | GET |  |
| [Update Segment](actions/update-segment.md) | PUT |  |

### Signup Form

| Action | Method | Description |
| --- | --- | --- |
| [List Signup Forms](actions/list-signup-forms.md) | GET | Retrieves signup form overviews from Maildroppa. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Count Filtered Subscribers](actions/count-filtered-subscribers.md) | GET | Counts Maildroppa subscribers by segment expression. |
| [Count Subscribers](actions/count-subscribers.md) | GET | Counts Maildroppa subscribers by status. |
| [Create Double Opt-In Subscriber](actions/create-double-opt-in-subscriber.md) | POST | Starts double opt-in for a new Maildroppa subscriber. |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in Maildroppa without double opt-in. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes a subscriber from Maildroppa by ID. |
| [Delete Subscriber By Email](actions/delete-subscriber-by-email.md) | DELETE | Deletes a subscriber from Maildroppa by email address. |
| [Delete Subscriber Field By Email](actions/delete-subscriber-field-by-email.md) | DELETE |  |
| [Delete Subscriber Field By ID](actions/delete-subscriber-field-by-id.md) | DELETE |  |
| [Delete Subscribers](actions/delete-subscribers.md) | DELETE | Deletes multiple subscribers from Maildroppa by ID. |
| [Delete Subscribers By Status](actions/delete-subscribers-by-status.md) | DELETE | Deletes all Maildroppa subscribers for a selected status. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from Maildroppa by ID. |
| [List Filtered Subscribers](actions/list-filtered-subscribers.md) | GET | Finds Maildroppa subscribers by segment expression. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from Maildroppa with pagination. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates a subscriber in Maildroppa without changing the email. |
| [Update Subscriber Email](actions/update-subscriber-email.md) | PUT | Updates a subscriber email address in Maildroppa. |
| [Upsert Subscriber Field By Email](actions/upsert-subscriber-field-by-email.md) | PUT |  |
| [Upsert Subscriber Field By ID](actions/upsert-subscriber-field-by-id.md) | PUT |  |

### Subscriber Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber Field](actions/create-subscriber-field.md) | POST |  |
| [Delete Subscriber Field](actions/delete-subscriber-field.md) | DELETE |  |
| [List Subscriber Fields](actions/list-subscriber-fields.md) | GET |  |
| [Update Subscriber Field](actions/update-subscriber-field.md) | PUT |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber Tag By Email](actions/add-subscriber-tag-by-email.md) | PUT |  |
| [Add Subscriber Tag By ID](actions/add-subscriber-tag-by-id.md) | PUT |  |
| [Create Tag](actions/create-tag.md) | POST |  |
| [Delete Subscriber Tag By Email](actions/delete-subscriber-tag-by-email.md) | DELETE |  |
| [Delete Subscriber Tag By ID](actions/delete-subscriber-tag-by-id.md) | DELETE |  |
| [Delete Tag](actions/delete-tag.md) | DELETE |  |
| [List Tags](actions/list-tags.md) | GET |  |
| [Update Tag](actions/update-tag.md) | PUT |  |

