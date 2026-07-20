# Campaign Refinery: Native API Reference

A consolidated summary of Campaign Refinery's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://developers.campaignrefinery.com/reference/api-summary
- **API base URL:** `https://app.campaignrefinery.com/rest`

## Authentication

### API Key

Use a Campaign Refinery provider-native API key from Settings > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.campaignrefinery.com/reference/oauth)

## API conventions

The total page count is read from `_metadata.page_count`. The current page number is read from `_metadata.page`.

## Pagination

Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `sort`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Form to Contact](actions/add-form-to-contact.md) | `POST /contacts/add-form` | [docs](https://developers.campaignrefinery.com/reference/add-form) |
| [Add Goal to Contact](actions/add-goal-to-contact.md) | `POST /contacts/add-goal` | [docs](https://developers.campaignrefinery.com/reference/add-goal) |
| [Add Tag to Contact](actions/add-tag-to-contact.md) | `POST /contacts/add-tag` | [docs](https://developers.campaignrefinery.com/reference/add-tag) |
| [Create Attribute](actions/create-attribute.md) | `POST /attributes/create-attribute` | [docs](https://developers.campaignrefinery.com/reference/create-attribute) |
| [Create Attribute Group](actions/create-attribute-group.md) | `POST /attributes/create-group` | [docs](https://developers.campaignrefinery.com/reference/create-group) |
| [Create Contact](actions/create-contact.md) | `POST /contacts/create-contact` | [docs](https://developers.campaignrefinery.com/reference/create-contact) |
| [Create Form](actions/create-form.md) | `POST /forms/create-form` | [docs](https://developers.campaignrefinery.com/reference/create-form) |
| [Create Goal](actions/create-goal.md) | `POST /goals/create-goal` | [docs](https://developers.campaignrefinery.com/reference/create-goal) |
| [Create Tag](actions/create-tag.md) | `POST /tags/create-tag` | [docs](https://developers.campaignrefinery.com/reference/create-tag) |
| [Delete Form](actions/delete-form.md) | `POST /forms/delete-form` | [docs](https://developers.campaignrefinery.com/reference/delete-form) |
| [Delete Tag from Contact](actions/delete-tag-from-contact.md) | `POST /contacts/delete-tag` | [docs](https://developers.campaignrefinery.com/reference/delete-tag) |
| [Export Points Balance CSV](actions/export-points-balance-csv.md) | `GET /gamification/get-points-balance` | [docs](https://developers.campaignrefinery.com/reference/csv-with-overall-points-balance-for-all-contacts) |
| [Get Attribute by Name](actions/get-attribute-by-name.md) | `GET /attributes/get-attribute` | [docs](https://developers.campaignrefinery.com/reference/get-attribute-by-name) |
| [Get Attribute Groups](actions/get-attribute-groups.md) | `GET /attributes/get-attribute-groups` | [docs](https://developers.campaignrefinery.com/reference/get-attribute-groups) |
| [Get Attributes](actions/get-attributes.md) | `GET /attributes/get-attributes` | [docs](https://developers.campaignrefinery.com/reference/get-attributes) |
| [Get Broadcast Stats](actions/get-broadcast-stats.md) | `POST /broadcasts/get_broadcast_stats` | [docs](https://developers.campaignrefinery.com/reference/get-broadcast-stats) |
| [Get Broadcasts](actions/get-broadcasts.md) | `GET /broadcasts/get_broadcasts` | [docs](https://developers.campaignrefinery.com/reference/get-broadcasts) |
| [Get Contact by Email](actions/get-contact-by-email.md) | `GET /contacts/get-contact` | [docs](https://developers.campaignrefinery.com/reference/get-contact) |
| [Get Contact Tags](actions/get-contact-tags.md) | `GET /contacts/get-contact-tags` | [docs](https://developers.campaignrefinery.com/reference/get-contact-tags) |
| [Get Contacts](actions/get-contacts.md) | `GET /contacts/get-contacts` | [docs](https://developers.campaignrefinery.com/reference/get-contacts) |
| [Get Daily Points](actions/get-daily-points.md) | `GET /gamification/get-daily-points` | [docs](https://developers.campaignrefinery.com/reference/get-the-daily-in-and-out-of-points) |
| [Get Form by Name](actions/get-form-by-name.md) | `GET /forms/get-form` | [docs](https://developers.campaignrefinery.com/reference/get-form-by-name) |
| [Get Forms](actions/get-forms.md) | `GET /forms/get-forms` | [docs](https://developers.campaignrefinery.com/reference/get-forms) |
| [Get Goal by ID](actions/get-goal-by-id.md) | `GET /goals/get-goal` | [docs](https://developers.campaignrefinery.com/reference/get-goal) |
| [Get Goal by Name](actions/get-goal-by-name.md) | `GET /goals/get-goal` | [docs](https://developers.campaignrefinery.com/reference/get-goal-by-name) |
| [Get Goals](actions/get-goals.md) | `GET /goals/get-goals` | [docs](https://developers.campaignrefinery.com/reference/get-goals) |
| [Get Tag by Name](actions/get-tag-by-name.md) | `GET /tags/get-tag` | [docs](https://developers.campaignrefinery.com/reference/get-tag-by-name) |
| [Get Tags](actions/get-tags.md) | `GET /tags/get-tags` | [docs](https://developers.campaignrefinery.com/reference/get-tags) |
| [Get Top Ranked Contacts](actions/get-top-ranked-contacts.md) | `GET /gamification/get-ranked-balance` | [docs](https://developers.campaignrefinery.com/reference/get-top-ranked-contacts) |
| [Subscribe Contact](actions/subscribe-contact.md) | `POST /contacts/subscribe` | [docs](https://developers.campaignrefinery.com/reference/subscribe-contact) |
| [Update Attribute](actions/update-attribute.md) | `POST /attributes/update-attribute` | [docs](https://developers.campaignrefinery.com/reference/update-attribute) |
| [Update Contact](actions/update-contact.md) | `POST /contacts/update-contact` | [docs](https://developers.campaignrefinery.com/reference/update-contact) |
| [Update Form](actions/update-form.md) | `POST /forms/update-form` | [docs](https://developers.campaignrefinery.com/reference/update-form) |
| [Update Goal](actions/update-goal.md) | `POST /goals/update-goal` | [docs](https://developers.campaignrefinery.com/reference/update-goal) |
| [Update Tag](actions/update-tag.md) | `POST /tags/update-tag` | [docs](https://developers.campaignrefinery.com/reference/update-tag) |
