# <img src="https://images.mindcloud.co/apps/icons/crowd-power_1774879312512.png" alt="CrowdPower logo" width="28" height="28"> CrowdPower: Universal API

Customer engagement platform for SaaS teams, with customer data, campaigns, segments, events, tags, and project automation workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/crowdPower/latest
- **Category:** Support / Customer Success
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://crowdpower.io
- **Vendor API docs:** https://documenter.getpostman.com/view/17896162/UV5TFKbh

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Project](actions/get-project.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Automation](actions/get-automation.md) | GET | Retrieves an automation from CrowdPower. |
| [Get Automations](actions/get-automations.md) | GET | Retrieves automations from CrowdPower. |
| [Get Broadcast](actions/get-broadcast.md) | GET | Retrieves a broadcast from CrowdPower. |
| [Get Broadcasts](actions/get-broadcasts.md) | GET | Retrieves broadcasts from CrowdPower. |

### Charges

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Charges](actions/get-customer-charges.md) | GET | Retrieves charges for a customer in CrowdPower. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from CrowdPower. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Trait](actions/get-trait.md) | GET | Retrieves a trait from CrowdPower. |
| [Get Traits](actions/get-traits.md) | GET | Retrieves traits from CrowdPower. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Add Notes](actions/add-notes.md) | PUT | Updates customer notes in CrowdPower. |
| [Create Customer with Email](actions/create-customer-with-email.md) | POST | Creates a customer in CrowdPower with an email address. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from CrowdPower. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from CrowdPower. |
| [Get Customers](actions/get-customers.md) | GET | Retrieves customers from CrowdPower. |
| [Unsubscribe from All Emails](actions/unsubscribe-from-all-emails.md) | PUT | Unsubscribes a customer from all emails in CrowdPower. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Events](actions/get-customer-events.md) | GET | Retrieves events for a customer in CrowdPower. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from CrowdPower. |
| [Get Events](actions/get-events.md) | GET | Retrieves events from CrowdPower. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Get Members](actions/get-members.md) | GET | Retrieves campaign members from CrowdPower. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Pages](actions/get-customer-pages.md) | GET | Retrieves pages for a customer in CrowdPower. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from CrowdPower. |
| [Get Projects](actions/get-projects.md) | GET | Retrieves projects for a company in CrowdPower. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in CrowdPower. |
| [Update Project Theme](actions/update-project-theme.md) | PUT | Updates a project theme in CrowdPower. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Get Segment](actions/get-segment.md) | GET | Retrieves a segment from CrowdPower. |
| [Get Segments](actions/get-segments.md) | GET | Retrieves segments from CrowdPower. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag](actions/add-tag.md) | POST | Adds a tag to a customer in CrowdPower. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from CrowdPower. |
| [Get Tags](actions/get-tags.md) | GET | Retrieves tags from CrowdPower. |
| [Remove Tag](actions/remove-tag.md) | DELETE | Removes a tag from a customer in CrowdPower. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Templates](actions/get-templates.md) | GET | Retrieves templates from CrowdPower. |

