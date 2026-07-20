# <img src="https://images.mindcloud.co/apps/icons/hypage-icon_1776722306333.png" alt="Hy.page logo" width="28" height="28"> Hy.page: Universal API

Hy.page is a creator commerce and bio-link platform for selling digital products, memberships, accepting donations and requests, collecting emails, and managing audience contacts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hypage/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hy.page
- **Vendor API docs:** https://platform.hyax.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List People](actions/list-people.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Book Meeting](actions/book-meeting.md) | POST |  |
| [List Meeting Slots](actions/list-meeting-slots.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Person](actions/create-or-update-person.md) | PUT |  |
| [Delete Person](actions/delete-person.md) | DELETE |  |
| [Get Person by Email](actions/get-person-by-email.md) | GET |  |
| [Get Person by ID](actions/get-person-by-id.md) | GET |  |
| [List People](actions/list-people.md) | GET |  |
| [Unsubscribe Person](actions/unsubscribe-person.md) | PUT |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Archive Post](actions/archive-post.md) | DELETE |  |
| [Create Post](actions/create-post.md) | POST |  |
| [Get Post](actions/get-post.md) | GET |  |
| [List Posts](actions/list-posts.md) | GET |  |
| [Update Post](actions/update-post.md) | PUT |  |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Enroll in Sequence](actions/enroll-in-sequence.md) | POST |  |
| [Send Transactional Email](actions/send-transactional-email.md) | POST |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Post Creation Job Status](actions/get-post-creation-job-status.md) | GET |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST |  |
| [Get Order](actions/get-order.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Add Tags](actions/add-tags.md) | PUT |  |
| [Remove Tags](actions/remove-tags.md) | PUT |  |

### Touchpoints

| Action | Method | Description |
| --- | --- | --- |
| [List Touchpoints](actions/list-touchpoints.md) | GET |  |

