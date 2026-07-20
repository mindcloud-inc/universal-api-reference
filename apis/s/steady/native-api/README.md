# Steady: Native API Reference

A consolidated summary of Steady's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://developers.steadyhq.com/
- **API base URL:** `https://steadyhq.com/api/v1`

## Authentication

### API Key

Authenticate with your Steady API key for publication-scoped REST endpoints such as /publication, /plans, and /subscriptions.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.steadyhq.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST /subscriptions/:subscription_id/cancel` | [docs](https://developers.steadyhq.com/#post-subscriptions-subscription_id-cancel) |
| [Create Audio Post](actions/create-audio-post.md) | `POST /posts/audio_posts` | [docs](https://developers.steadyhq.com/#creating-a-post) |
| [Delete Audio Post](actions/delete-audio-post.md) | `DELETE /posts/audio_posts/:post_id` | [docs](https://developers.steadyhq.com/#deleting-a-post) |
| [Get Publication](actions/get-publication.md) | `GET /publication` | [docs](https://developers.steadyhq.com/#get-publication) |
| [List Active Subscriptions](actions/list-active-subscriptions.md) | `GET /subscriptions` | [docs](https://developers.steadyhq.com/#get-subscriptions) |
| [List Inactive Subscriptions](actions/list-inactive-subscriptions.md) | `GET /subscriptions/inactive` | [docs](https://developers.steadyhq.com/#get-subscriptions-inactive) |
| [List Newsletter Subscribers](actions/list-newsletter-subscribers.md) | `GET /newsletter_subscribers` | [docs](https://developers.steadyhq.com/#get-newsletter_subscribers) |
| [List Plans](actions/list-plans.md) | `GET /plans` | [docs](https://developers.steadyhq.com/#get-plans) |
| [List Plans for Access Control](actions/list-plans-for-access-control.md) | `GET /posts/plans_for_access_control` | [docs](https://developers.steadyhq.com/#listing-plans-with-access) |
| [Send Double Opt-In Email](actions/send-double-opt-in-email.md) | `POST /newsletter_subscribers/send_double_opt_in_email` | [docs](https://developers.steadyhq.com/#post-newsletter_subscribers-send_double_opt_in_email) |
| [Update Audio Post](actions/update-audio-post.md) | `PUT /posts/audio_posts/:post_id` | [docs](https://developers.steadyhq.com/#updating-a-post) |
