# <img src="https://images.mindcloud.co/apps/icons/campaign-refinery_1776802662900.png" alt="Campaign Refinery logo" width="28" height="28"> Campaign Refinery: Universal API

Email marketing and automation platform for contacts, tags, goals, forms, broadcasts, and API-driven email utilities.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/campaignRefinery/latest
- **Category:** Marketing
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://campaignrefinery.com/
- **Vendor API docs:** https://developers.campaignrefinery.com/reference/api-summary

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contacts](actions/get-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Create Attribute](actions/create-attribute.md) | POST | Creates a new attribute in Campaign Refinery. |
| [Get Attribute by Name](actions/get-attribute-by-name.md) | GET | Retrieves an attribute by name from Campaign Refinery. |
| [Get Attributes](actions/get-attributes.md) | GET | Retrieves all attributes from Campaign Refinery. |
| [Update Attribute](actions/update-attribute.md) | PUT | Updates an existing attribute in Campaign Refinery. |

### Attribute Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Attribute Group](actions/create-attribute-group.md) | POST | Creates a new attribute group in Campaign Refinery. |
| [Get Attribute Groups](actions/get-attribute-groups.md) | GET | Retrieves attribute groups from Campaign Refinery. |

### Broadcast

| Action | Method | Description |
| --- | --- | --- |
| [Get Broadcasts](actions/get-broadcasts.md) | GET | Retrieves all broadcasts from Campaign Refinery. |

### Broadcast Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Broadcast Stats](actions/get-broadcast-stats.md) | GET | Retrieves broadcast stats from Campaign Refinery. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Form to Contact](actions/add-form-to-contact.md) | PUT | Adds a form to a contact in Campaign Refinery. |
| [Add Goal to Contact](actions/add-goal-to-contact.md) | PUT | Adds a goal to a contact in Campaign Refinery. |
| [Add Tag to Contact](actions/add-tag-to-contact.md) | PUT | Adds a tag to a contact in Campaign Refinery. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Campaign Refinery. |
| [Get Contact by Email](actions/get-contact-by-email.md) | GET | Retrieves a contact by email from Campaign Refinery. |
| [Get Contacts](actions/get-contacts.md) | GET | Retrieves all contacts from Campaign Refinery. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Campaign Refinery. |

### Contact Ranking

| Action | Method | Description |
| --- | --- | --- |
| [Get Top Ranked Contacts](actions/get-top-ranked-contacts.md) | GET | Retrieves top ranked contacts from Campaign Refinery. |

### Contact Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe Contact](actions/subscribe-contact.md) | POST | Subscribes an existing contact in Campaign Refinery. |

### Contact Tag Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Tag from Contact](actions/delete-tag-from-contact.md) | DELETE | Deletes a tag from a contact in Campaign Refinery. |

### Daily Points

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Points](actions/get-daily-points.md) | GET | Retrieves daily points from Campaign Refinery. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in Campaign Refinery. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes an existing form from Campaign Refinery. |
| [Get Form by Name](actions/get-form-by-name.md) | GET | Retrieves a form by name from Campaign Refinery. |
| [Get Forms](actions/get-forms.md) | GET | Retrieves all forms from Campaign Refinery. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in Campaign Refinery. |

### Goal

| Action | Method | Description |
| --- | --- | --- |
| [Create Goal](actions/create-goal.md) | POST | Creates a new goal in Campaign Refinery. |
| [Get Goal by ID](actions/get-goal-by-id.md) | GET | Retrieves a goal by ID from Campaign Refinery. |
| [Get Goal by Name](actions/get-goal-by-name.md) | GET | Retrieves a goal by name from Campaign Refinery. |
| [Get Goals](actions/get-goals.md) | GET | Retrieves all goals from Campaign Refinery. |
| [Update Goal](actions/update-goal.md) | PUT | Updates an existing goal in Campaign Refinery. |

### Points Balance Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Points Balance CSV](actions/export-points-balance-csv.md) | GET | Retrieves the points balance CSV from Campaign Refinery. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Campaign Refinery. |
| [Get Contact Tags](actions/get-contact-tags.md) | GET | Retrieves tags for a contact from Campaign Refinery. |
| [Get Tag by Name](actions/get-tag-by-name.md) | GET | Retrieves a tag by name from Campaign Refinery. |
| [Get Tags](actions/get-tags.md) | GET | Retrieves all tags from Campaign Refinery. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Campaign Refinery. |

