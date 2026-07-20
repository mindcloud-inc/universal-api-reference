# <img src="https://images.mindcloud.co/apps/icons/reteach_1774555257414.png" alt="Reteach logo" width="28" height="28"> Reteach: Universal API

Reteach is a learning platform for building academies, managing courses, and organizing participant learning experiences.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reteach/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.reteach.com/
- **Vendor API docs:** https://api.reteach.io/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Customer](actions/get-customer.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerIdentifier=2bf64377-4a26-4439-9c69-323b9111ea70" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Academy

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Academy](actions/get-current-academy.md) | GET |  |

### Course

| Action | Method | Description |
| --- | --- | --- |
| [Get Course](actions/get-course.md) | GET |  |
| [List Courses](actions/list-courses.md) | GET |  |

### Course Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Get Course Invitation](actions/get-course-invitation.md) | GET |  |
| [List Course Invitations](actions/list-course-invitations.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |

### Customer Course Certificate

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Course Certificates](actions/list-customer-course-certificates.md) | GET |  |

### Customer Export

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Export](actions/get-customer-export.md) | GET |  |
| [List Customer Exports](actions/list-customer-exports.md) | GET |  |

### Customer Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Group](actions/get-customer-group.md) | GET |  |
| [List Customer Groups](actions/list-customer-groups.md) | GET |  |

### Customer Import

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Import](actions/get-customer-import.md) | GET |  |
| [List Customer Imports](actions/list-customer-imports.md) | GET |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get E-Commerce Order](actions/get-e-commerce-order.md) | GET |  |
| [List E-Commerce Orders](actions/list-e-commerce-orders.md) | GET |  |

### Participation

| Action | Method | Description |
| --- | --- | --- |
| [Get Participation](actions/get-participation.md) | GET |  |
| [List Participations](actions/list-participations.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

