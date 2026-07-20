# <img src="https://images.mindcloud.co/apps/icons/beehiiv_1772719508774.png" alt="Beehiiv logo" width="28" height="28"> Beehiiv: Universal API

Publish newsletters, grow audiences, monetize content, and track performance.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/beehiiv/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.beehiiv.com
- **Vendor API docs:** https://developers.beehiiv.com/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Publications](actions/list-publications.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-publications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Bulk Subscription Update

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Subscription Update](actions/get-bulk-subscription-update.md) | GET | Retrieves a bulk subscription update from Beehiiv. |
| [List Bulk Subscription Updates](actions/list-bulk-subscription-updates.md) | GET | Retrieves bulk subscription updates from Beehiiv. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Publication Custom Fields](actions/list-publication-custom-fields.md) | GET | Retrieves publication custom fields from Beehiiv. |

### Email Blast

| Action | Method | Description |
| --- | --- | --- |
| [Get Publication Email Blast](actions/get-publication-email-blast.md) | GET | Retrieves an email blast for a publication from Beehiiv. |
| [List Publication Email Blasts](actions/list-publication-email-blasts.md) | GET | Retrieves email blasts for a publication from Beehiiv. |

### Engagement

| Action | Method | Description |
| --- | --- | --- |
| [List Publication Engagements](actions/list-publication-engagements.md) | GET | Retrieves publication engagements from Beehiiv. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Publication Post](actions/create-publication-post.md) | POST | Creates a publication post in Beehiiv. |
| [Delete Publication Post](actions/delete-publication-post.md) | DELETE | Deletes a publication post from Beehiiv. |
| [Get Publication Post](actions/get-publication-post.md) | GET | Retrieves a publication post from Beehiiv. |
| [Get Publication Post Aggregate Stats](actions/get-publication-post-aggregate-stats.md) | GET | Retrieves aggregate stats for publication posts from Beehiiv. |
| [List Publication Posts](actions/list-publication-posts.md) | GET | Retrieves publication posts from Beehiiv. |

### Publication

| Action | Method | Description |
| --- | --- | --- |
| [Get Publication](actions/get-publication.md) | GET | Retrieves a publication from Beehiiv. |
| [List Publications](actions/list-publications.md) | GET | Retrieves publications from Beehiiv. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a subscription in Beehiiv. |
| [Delete Subscription](actions/delete-subscription.md) | DELETE | Deletes a subscription from Beehiiv. |
| [Get Subscription by Email](actions/get-subscription-by-email.md) | GET | Retrieves a subscription from Beehiiv by email address. |
| [Get Subscription by ID](actions/get-subscription-by-id.md) | GET | Retrieves a subscription from Beehiiv by ID. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Beehiiv. |
| [Update Subscription by Email](actions/update-subscription-by-email.md) | PUT | Updates a subscription in Beehiiv by email address. |
| [Update Subscription by ID](actions/update-subscription-by-id.md) | PUT | Updates a subscription in Beehiiv by ID. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscription Tag](actions/add-subscription-tag.md) | PUT | Adds tags to a subscription in Beehiiv. |
| [Bulk Create Subscriptions](actions/bulk-create-subscriptions.md) | POST | Creates subscriptions in bulk in Beehiiv. |
| [Get Subscription by Subscriber ID](actions/get-subscription-by-subscriber-id.md) | GET | Retrieves a subscription from Beehiiv by subscriber ID. |
| [Get Subscription JWT Token](actions/get-subscription-jwt-token.md) | GET | Generates a subscription JWT token in Beehiiv. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Publication Webhook](actions/create-publication-webhook.md) | POST | Creates a publication webhook in Beehiiv. |
| [Delete Publication Webhook](actions/delete-publication-webhook.md) | DELETE | Deletes a publication webhook from Beehiiv. |
| [Get Publication Webhook](actions/get-publication-webhook.md) | GET | Retrieves a publication webhook from Beehiiv. |
| [List Publication Webhooks](actions/list-publication-webhooks.md) | GET | Retrieves publication webhooks from Beehiiv. |
| [Update Publication Webhook](actions/update-publication-webhook.md) | PUT | Updates a publication webhook in Beehiiv. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Identify Workspace](actions/identify-workspace.md) | GET | Retrieves the current workspace from Beehiiv. |

