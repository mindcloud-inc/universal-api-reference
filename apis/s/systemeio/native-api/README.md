# Systeme.io: Native API Reference

A consolidated summary of Systeme.io's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://developer.systeme.io/reference/api
- **API base URL:** `https://api.systeme.io`

## Authentication

### API Key

Systeme.io Public API key authentication via X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://help.systeme.io/article/672-where-can-i-find-my-systeme-io-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `items`.

## Pagination

Use `limit` in the query string to set the page size (accepted range 10–100). Use `startingAfter` in the query string as the pagination cursor.

## Sorting

Set the sort field with `order` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Tag](actions/add-contact-tag.md) | `POST /api/contacts/:id/tags` | [docs](https://developer.systeme.io/reference/post_contact_tag-1) |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST /api/payment/subscriptions/:id/cancel` | [docs](https://developer.systeme.io/reference/cancel_subscription-1) |
| [Create Community Membership](actions/create-community-membership.md) | `POST /api/community/communities/:communityId/memberships` | [docs](https://developer.systeme.io/reference/api_communitycommunities_communityidmemberships_post-1) |
| [Create Contact](actions/create-contact.md) | `POST /api/contacts` | [docs](https://developer.systeme.io/reference/post_contact-1) |
| [Create Contact Field](actions/create-contact-field.md) | `POST /api/contact_fields` | [docs](https://developer.systeme.io/reference/api_contact_fields_post-1) |
| [Create Course Enrollment](actions/create-course-enrollment.md) | `POST /api/school/courses/:courseId/enrollments` | [docs](https://developer.systeme.io/reference/api_schoolcourses_courseidenrollments_post-1) |
| [Create Tag](actions/create-tag.md) | `POST /api/tags` | [docs](https://developer.systeme.io/reference/api_tags_post-1) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/webhooks` | [docs](https://developer.systeme.io/reference/api_webhooks_post-1) |
| [Delete Community Membership](actions/delete-community-membership.md) | `DELETE /api/community/memberships/:id` | [docs](https://developer.systeme.io/reference/api_communitymemberships_id_delete-1) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /api/contacts/:id` | [docs](https://developer.systeme.io/reference/delete_contact-1) |
| [Delete Contact Field](actions/delete-contact-field.md) | `DELETE /api/contact_fields/:slug` | [docs](https://developer.systeme.io/reference/api_contact_fields_slug_delete-1) |
| [Delete Enrollment](actions/delete-enrollment.md) | `DELETE /api/school/enrollments/:id` | [docs](https://developer.systeme.io/reference/api_schoolenrollments_id_delete-1) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /api/tags/:id` | [docs](https://developer.systeme.io/reference/api_tags_id_delete-1) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/webhooks/:id` | [docs](https://developer.systeme.io/reference/api_webhooks_id_delete-1) |
| [Get Contact](actions/get-contact.md) | `GET /api/contacts/:id` | [docs](https://developer.systeme.io/reference/api_contacts_id_get-1) |
| [Get Tag](actions/get-tag.md) | `GET /api/tags/:id` | [docs](https://developer.systeme.io/reference/api_tags_id_get-1) |
| [Get Webhook](actions/get-webhook.md) | `GET /api/webhooks/:id` | [docs](https://developer.systeme.io/reference/api_webhooks_id_get-1) |
| [List Communities](actions/list-communities.md) | `GET /api/community/communities` | [docs](https://developer.systeme.io/reference/api_communitycommunities_get_collection-1) |
| [List Community Memberships](actions/list-community-memberships.md) | `GET /api/community/memberships` | [docs](https://developer.systeme.io/reference/api_communitymemberships_get_collection-1) |
| [List Contact Fields](actions/list-contact-fields.md) | `GET /api/contact_fields` | [docs](https://developer.systeme.io/reference/api_contact_fields_get_collection-1) |
| [List Contacts](actions/list-contacts.md) | `GET /api/contacts` | [docs](https://developer.systeme.io/reference/api_contacts_get_collection-1) |
| [List Courses](actions/list-courses.md) | `GET /api/school/courses` | [docs](https://developer.systeme.io/reference/api_schoolcourses_get_collection-1) |
| [List Enrollments](actions/list-enrollments.md) | `GET /api/school/enrollments` | [docs](https://developer.systeme.io/reference/api_schoolenrollments_get_collection-1) |
| [List Payment Subscriptions](actions/list-payment-subscriptions.md) | `GET /api/payment/subscriptions` | [docs](https://developer.systeme.io/reference/api_paymentsubscriptions_get_collection-1) |
| [List Tags](actions/list-tags.md) | `GET /api/tags` | [docs](https://developer.systeme.io/reference/api_tags_get_collection-1) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/webhooks` | [docs](https://developer.systeme.io/reference/api_webhooks_get_collection-1) |
| [Remove Contact Tag](actions/remove-contact-tag.md) | `DELETE /api/contacts/:id/tags/:tagId` | [docs](https://developer.systeme.io/reference/delete_contact_tag-1) |
| [Update Contact](actions/update-contact.md) | `PATCH /api/contacts/:id` | [docs](https://developer.systeme.io/reference/api_contacts_id_patch-1) |
| [Update Contact Field](actions/update-contact-field.md) | `PATCH /api/contact_fields/:slug` | [docs](https://developer.systeme.io/reference/api_contact_fields_slug_patch-1) |
| [Update Tag](actions/update-tag.md) | `PUT /api/tags/:id` | [docs](https://developer.systeme.io/reference/api_tags_id_put-1) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /api/webhooks/:id` | [docs](https://developer.systeme.io/reference/api_webhooks_id_patch-1) |
