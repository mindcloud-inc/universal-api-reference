# <img src="https://images.mindcloud.co/apps/icons/systemeio_1772654914789.png" alt="Systeme.io logo" width="28" height="28"> Systeme.io: Universal API

Build funnels, send campaigns, automate marketing, and sell courses.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/systemeio/latest
- **Category:** Marketing
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://systeme.io
- **Vendor API docs:** https://developer.systeme.io/reference/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tags](actions/list-tags.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-tags?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Community

| Action | Method | Description |
| --- | --- | --- |
| [List Communities](actions/list-communities.md) | GET | Retrieves the collection of communities from Systeme.io. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Tag](actions/add-contact-tag.md) | PUT | Assigns a tag to a contact in Systeme.io. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Systeme.io. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Systeme.io. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact resource from Systeme.io. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves the collection of contacts from Systeme.io. |
| [Remove Contact Tag](actions/remove-contact-tag.md) | DELETE | Removes a tag from a contact in Systeme.io. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Systeme.io. |

### Contact Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Field](actions/create-contact-field.md) | POST | Creates a contact field in Systeme.io. |
| [Delete Contact Field](actions/delete-contact-field.md) | DELETE | Deletes an existing contact field from Systeme.io. |
| [List Contact Fields](actions/list-contact-fields.md) | GET | Retrieves the collection of contact fields from Systeme.io. |
| [Update Contact Field](actions/update-contact-field.md) | PUT | Updates an existing contact field in Systeme.io. |

### Course

| Action | Method | Description |
| --- | --- | --- |
| [List Courses](actions/list-courses.md) | GET | Retrieves the collection of courses from Systeme.io. |

### Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Create Course Enrollment](actions/create-course-enrollment.md) | POST | Creates a course enrollment in Systeme.io. |
| [Delete Enrollment](actions/delete-enrollment.md) | DELETE | Deletes an existing enrollment from Systeme.io. |
| [List Enrollments](actions/list-enrollments.md) | GET | Retrieves the collection of enrollments from Systeme.io. |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [Create Community Membership](actions/create-community-membership.md) | POST | Creates a membership in a Systeme.io community. |
| [Delete Community Membership](actions/delete-community-membership.md) | DELETE | Deletes an existing community membership from Systeme.io. |
| [List Community Memberships](actions/list-community-memberships.md) | GET | Retrieves the collection of community memberships from Systeme.io. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT | Cancels an existing subscription in Systeme.io. |
| [List Payment Subscriptions](actions/list-payment-subscriptions.md) | GET | Retrieves payment subscriptions from Systeme.io for a contact. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Systeme.io. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Systeme.io. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag resource from Systeme.io. |
| [List Tags](actions/list-tags.md) | GET | Retrieves the collection of tags from Systeme.io. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Systeme.io. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Systeme.io. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Systeme.io. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook resource from Systeme.io. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves the collection of webhooks from Systeme.io. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Systeme.io. |

