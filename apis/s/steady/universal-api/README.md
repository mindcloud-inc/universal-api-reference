# <img src="https://images.mindcloud.co/apps/icons/steady_1773846065132.png" alt="Steady logo" width="28" height="28"> Steady: Universal API

Use Steady OAuth2 for member-scoped endpoints like /users/me and /subscriptions/me, and use the Steady API key for publication-scoped REST endpoints like /publication, /plans, and /subscriptions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/steady/latest
- **Category:** Marketing / Social Media
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://steadyhq.com
- **Vendor API docs:** https://developers.steadyhq.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Publication](actions/get-publication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/steady/latest/actions/get-publication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Audio Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Audio Post](actions/create-audio-post.md) | POST | Creates a new audio post in Steady. |
| [Delete Audio Post](actions/delete-audio-post.md) | DELETE | Deletes an existing audio post from Steady. |
| [Update Audio Post](actions/update-audio-post.md) | PUT | Updates an existing audio post in Steady. |

### Newsletter Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [List Newsletter Subscribers](actions/list-newsletter-subscribers.md) | GET | Retrieves newsletter subscribers for a Steady publication. |
| [Send Double Opt-In Email](actions/send-double-opt-in-email.md) | POST | Sends a double opt-in email from Steady. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Plans](actions/list-plans.md) | GET | Retrieves membership plans for a Steady publication. |
| [List Plans for Access Control](actions/list-plans-for-access-control.md) | GET | Retrieves plans for post access control in Steady. |

### Publication

| Action | Method | Description |
| --- | --- | --- |
| [Get Publication](actions/get-publication.md) | GET | Retrieves publication details for a Steady publication. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT | Cancels a Steady subscription at the current term's end. |
| [List Active Subscriptions](actions/list-active-subscriptions.md) | GET | Retrieves active subscriptions for a Steady publication. |
| [List Inactive Subscriptions](actions/list-inactive-subscriptions.md) | GET | Retrieves inactive subscriptions for a Steady publication. |

