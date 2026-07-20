# <img src="https://images.mindcloud.co/apps/icons/kit_1772206549090.png" alt="Kit logo" width="28" height="28"> Kit: Universal API

Kit, formerly ConvertKit, is an email marketing platform for creators to manage subscribers, tags, forms, sequences, broadcasts, and audience growth automation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kit/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kit.com
- **Vendor API docs:** https://developers.kit.com/api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Broadcast](actions/get-broadcast.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kit/latest/actions/get-broadcast?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves current account details from Kit. |

### Broadcast

| Action | Method | Description |
| --- | --- | --- |
| [Create Broadcast](actions/create-broadcast.md) | POST | Creates a new broadcast in Kit. |
| [Get Broadcast](actions/get-broadcast.md) | GET | Retrieves a broadcast record from Kit. |
| [List Broadcasts](actions/list-broadcasts.md) | GET | Lists broadcasts in your Kit account. |
| [Update Broadcast](actions/update-broadcast.md) | PUT | Updates an existing broadcast in Kit. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in Kit. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Lists custom fields in your Kit account. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET | Lists forms in your Kit account. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [List Segments](actions/list-segments.md) | GET | Lists segments in your Kit account. |

### Sequence

| Action | Method | Description |
| --- | --- | --- |
| [List Sequences](actions/list-sequences.md) | GET | Lists sequences in your Kit account. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber to Form](actions/add-subscriber-to-form.md) | POST | Adds an existing subscriber to a Kit form. |
| [Add Subscriber to Sequence](actions/add-subscriber-to-sequence.md) | POST | Adds an existing subscriber to a Kit sequence. |
| [Add Tag to Subscriber](actions/add-tag-to-subscriber.md) | PUT | Adds a tag to a Kit subscriber. |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in Kit. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber record from Kit. |
| [List Form Subscribers](actions/list-form-subscribers.md) | GET | Lists subscribers for a Kit form. |
| [List Sequence Subscribers](actions/list-sequence-subscribers.md) | GET | Lists subscribers for a Kit sequence. |
| [List Subscribers](actions/list-subscribers.md) | GET | Lists subscribers in your Kit account. |
| [Remove Tag From Subscriber](actions/remove-tag-from-subscriber.md) | DELETE | Removes a tag from a Kit subscriber. |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | PUT | Unsubscribes an existing subscriber in Kit. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in Kit. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Kit. |
| [List Tags](actions/list-tags.md) | GET | Lists tags in your Kit account. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Tags for Subscriber](actions/list-tags-for-subscriber.md) | GET | Lists tags for a Kit subscriber. |

