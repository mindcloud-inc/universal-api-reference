# CrowdPower: Native API Reference

A consolidated summary of CrowdPower's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/17896162/UV5TFKbh
- **API base URL:** `https://api.crowdpower.io/v1`

## Authentication

### API Key

Authenticate with your CrowdPower project secret key.

### Credentials

- **API Key:** `apiKey` · required
- **Project ID:** `projectId` · required · Your CrowdPower project ID.
- **Company ID:** `companyId` · optional · Your CrowdPower company ID.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documenter.getpostman.com/view/17896162/UV5TFKbh)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Notes](actions/add-notes.md) | `PUT customers/:customer_id/notes` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Add Tag](actions/add-tag.md) | `POST customers/:customer_id/tags` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Create Customer with Email](actions/create-customer-with-email.md) | `POST projects/{{credentials.projectId}}/customers` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Delete Customer](actions/delete-customer.md) | `DELETE customers/:customer_id` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Automation](actions/get-automation.md) | `GET campaigns/:campaign_id` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Automations](actions/get-automations.md) | `GET projects/{{credentials.projectId}}/campaigns` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Broadcast](actions/get-broadcast.md) | `GET campaigns/:campaign_id` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Broadcasts](actions/get-broadcasts.md) | `GET projects/{{credentials.projectId}}/campaigns` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Company](actions/get-company.md) | `GET companies/:company_id` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Customer](actions/get-customer.md) | `GET customers/:customer_id` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Customer Charges](actions/get-customer-charges.md) | `GET customers/:customer_id/charges` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Customer Events](actions/get-customer-events.md) | `GET customers/:customer_id/events` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Customer Pages](actions/get-customer-pages.md) | `GET customers/:customer_id/pages` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Customers](actions/get-customers.md) | `GET projects/{{credentials.projectId}}/customers` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Event](actions/get-event.md) | `GET events/:event_id` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Events](actions/get-events.md) | `GET projects/{{credentials.projectId}}/events` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Members](actions/get-members.md) | `GET campaigns/:campaign_id/members` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Project](actions/get-project.md) | `GET projects/{{credentials.projectId}}` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Projects](actions/get-projects.md) | `GET companies/:company_id/projects` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Segment](actions/get-segment.md) | `GET segments/:segment_id` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Segments](actions/get-segments.md) | `GET projects/{{credentials.projectId}}/segments` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Tag](actions/get-tag.md) | `GET tags/:tag_id` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Tags](actions/get-tags.md) | `GET projects/{{credentials.projectId}}/tags` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Templates](actions/get-templates.md) | `GET projects/{{credentials.projectId}}/templates` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Trait](actions/get-trait.md) | `GET traits/:trait_id` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Get Traits](actions/get-traits.md) | `GET projects/{{credentials.projectId}}/traits` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Remove Tag](actions/remove-tag.md) | `DELETE customers/:customer_id/tags` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Unsubscribe from All Emails](actions/unsubscribe-from-all-emails.md) | `PUT customers/:customer_id/unsubscribe` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Update Project](actions/update-project.md) | `PUT projects/{{credentials.projectId}}` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
| [Update Project Theme](actions/update-project-theme.md) | `PUT projects/{{credentials.projectId}}/theme` | [docs](https://documenter.getpostman.com/view/17896162/UV5TFKbh) |
