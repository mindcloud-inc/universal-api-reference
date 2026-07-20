# <img src="https://images.mindcloud.co/apps/icons/mailchimp_1772734172730.png" alt="Mailchimp logo" width="28" height="28"> Mailchimp: Universal API

Manage audiences, create campaigns, automate emails, and track engagement.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailChimp/latest
- **Category:** Marketing
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mailchimp.com/
- **Vendor API docs:** https://mailchimp.com/developer/marketing/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Audiences](actions/list-audiences.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audiences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Audience

| Action | Method | Description |
| --- | --- | --- |
| [Add Audience](actions/add-audience.md) | POST | Creates a new audience in Mailchimp. |
| [Get Audience](actions/get-audience.md) | GET | Retrieves an audience from Mailchimp. |
| [List Audiences](actions/list-audiences.md) | GET | Retrieves audiences from Mailchimp. |
| [Update Audience](actions/update-audience.md) | PUT | Updates an existing audience in Mailchimp. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Mailchimp. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Mailchimp. |
| [Get Campaign Content](actions/get-campaign-content.md) | GET | Retrieves campaign content from Mailchimp. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Mailchimp. |
| [Schedule Campaign](actions/schedule-campaign.md) | PUT | Schedules a campaign in Mailchimp. |
| [Send Campaign](actions/send-campaign.md) | PUT | Sends a campaign from Mailchimp. |
| [Set Campaign Content](actions/set-campaign-content.md) | PUT | Updates campaign content in Mailchimp. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Mailchimp. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Add Customer](actions/add-customer.md) | POST | Creates a new customer in a Mailchimp e-commerce store. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from a Mailchimp e-commerce store. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from a Mailchimp e-commerce store. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from a Mailchimp e-commerce store. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in a Mailchimp e-commerce store. |
| [Upsert Customer](actions/upsert-customer.md) | PUT | Creates or updates a customer in a Mailchimp e-commerce store. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Audience Member](actions/add-audience-member.md) | POST | Creates a new member in a Mailchimp audience. |
| [Archive Audience Member](actions/archive-audience-member.md) | DELETE | Archives a member in a Mailchimp audience. |
| [Get Audience Member](actions/get-audience-member.md) | GET | Retrieves a member from a Mailchimp audience. |
| [List Audience Members](actions/list-audience-members.md) | GET | Retrieves members from a Mailchimp audience. |
| [Update Audience Member](actions/update-audience-member.md) | PUT | Updates an existing member in a Mailchimp audience. |
| [Upsert Audience Member](actions/upsert-audience-member.md) | PUT | Finds a member in Mailchimp, or creates one if no match is found. |

### Mergefield

| Action | Method | Description |
| --- | --- | --- |
| [Add Merge Field](actions/add-merge-field.md) | POST | Creates a new merge field in a Mailchimp audience. |
| [List Merge Fields](actions/list-merge-fields.md) | GET | Retrieves merge fields from a Mailchimp audience. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Report](actions/get-campaign-report.md) | GET | Retrieves a campaign report from Mailchimp. |
| [List Reports](actions/list-reports.md) | GET | Retrieves campaign reports from Mailchimp. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Add Audience Segment](actions/add-audience-segment.md) | POST | Creates a new segment in a Mailchimp audience. |
| [Get Audience Segment](actions/get-audience-segment.md) | GET | Retrieves a segment from a Mailchimp audience. |
| [List Audience Segments](actions/list-audience-segments.md) | GET | Retrieves segments from a Mailchimp audience. |
| [Update Audience Segment](actions/update-audience-segment.md) | PUT | Updates an existing segment in a Mailchimp audience. |

### Store

| Action | Method | Description |
| --- | --- | --- |
| [Add E-commerce Store](actions/add-e-commerce-store.md) | POST | Creates a new e-commerce store in Mailchimp. |
| [Delete E-commerce Store](actions/delete-e-commerce-store.md) | DELETE | Deletes an existing e-commerce store from Mailchimp. |
| [Get E-commerce Store](actions/get-e-commerce-store.md) | GET | Retrieves an e-commerce store from Mailchimp. |
| [List E-commerce Stores](actions/list-e-commerce-stores.md) | GET | Retrieves e-commerce stores from Mailchimp. |
| [Update E-commerce Store](actions/update-e-commerce-store.md) | PUT | Updates an existing e-commerce store in Mailchimp. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Member Tags](actions/list-member-tags.md) | GET | Retrieves tags for a member from a Mailchimp audience. |
| [Update Member Tags](actions/update-member-tags.md) | PUT | Updates tags for a member in a Mailchimp audience. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Mailchimp. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Mailchimp. |

