# <img src="https://images.mindcloud.co/apps/icons/fingertip_1775760014678.png" alt="Fingertip logo" width="28" height="28"> Fingertip: Universal API

Manage bookings, invoices, forms, and products

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fingertip/latest
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fingertip.com
- **Vendor API docs:** https://docs.fingertip.com/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Health Check](actions/get-health-check.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/get-health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Block

| Action | Method | Description |
| --- | --- | --- |
| [Create Block](actions/create-block.md) | POST |  |
| [List Blocks](actions/list-blocks.md) | GET |  |

### Blog Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Blog Post](actions/get-blog-post.md) | GET |  |
| [List Blog Posts](actions/list-blog-posts.md) | GET |  |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [List Bookings](actions/list-bookings.md) | GET |  |

### Event Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Type](actions/get-event-type.md) | GET |  |
| [List Event Types](actions/list-event-types.md) | GET |  |

### Form Response

| Action | Method | Description |
| --- | --- | --- |
| [List Form Responses](actions/list-form-responses.md) | GET |  |

### Form Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Template](actions/get-form-template.md) | GET |  |
| [List Form Templates](actions/list-form-templates.md) | GET |  |

### Health Check

| Action | Method | Description |
| --- | --- | --- |
| [Get Health Check](actions/get-health-check.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Delete Page](actions/delete-page.md) | DELETE |  |
| [Delete Site](actions/delete-site.md) | DELETE |  |
| [List Sites](actions/list-sites.md) | GET |  |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST |  |
| [Get Page](actions/get-page.md) | GET |  |
| [List Pages](actions/list-pages.md) | GET |  |
| [Update Page](actions/update-page.md) | PUT |  |

### Page Theme

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Theme](actions/get-page-theme.md) | GET |  |
| [Update Page Theme](actions/update-page-theme.md) | PUT |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST |  |
| [Get Site](actions/get-site.md) | GET |  |
| [Update Site](actions/update-site.md) | PUT |  |

### Site Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Analytics](actions/get-site-analytics.md) | GET |  |

### Site Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Site Contact](actions/create-site-contact.md) | POST |  |
| [List Site Contacts](actions/list-site-contacts.md) | GET |  |

### Site Membership

| Action | Method | Description |
| --- | --- | --- |
| [Create Site Membership](actions/create-site-membership.md) | POST |  |
| [List Site Memberships](actions/list-site-memberships.md) | GET |  |
| [Update Site Membership](actions/update-site-membership.md) | PUT |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET |  |
| [List Workspaces](actions/list-workspaces.md) | GET |  |
| [Update Workspace](actions/update-workspace.md) | PUT |  |

