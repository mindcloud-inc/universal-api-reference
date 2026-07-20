# <img src="https://images.mindcloud.co/apps/icons/instasent_1774635772987.png" alt="Instasent logo" width="28" height="28"> Instasent: Universal API

Instasent is an SMS marketing and audience engagement platform for managing projects, audiences, data sources, and direct SMS delivery.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/instasent/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://instasent.com/
- **Vendor API docs:** https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Audiences

| Action | Method | Description |
| --- | --- | --- |
| [Aggregate Audience](actions/aggregate-audience.md) | GET |  |
| [Get Audience Contact](actions/get-audience-contact.md) | GET |  |
| [Get Audience Contact by User ID](actions/get-audience-contact-by-user-id.md) | GET |  |
| [Get Project Attribute Specs](actions/get-project-attribute-specs.md) | GET |  |
| [Scroll Audience](actions/scroll-audience.md) | GET |  |
| [Search Audience](actions/search-audience.md) | GET |  |
| [Search Audience by Email](actions/search-audience-by-email.md) | GET |  |
| [Search Audience by Phone](actions/search-audience-by-phone.md) | GET |  |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Create Datasource](actions/create-datasource.md) | POST |  |
| [Delete Stream Record](actions/delete-stream-record.md) | DELETE |  |
| [Get Datasource](actions/get-datasource.md) | GET |  |
| [Get Datasource Stats](actions/get-datasource-stats.md) | GET |  |
| [Get Datasource Stream](actions/get-datasource-stream.md) | GET |  |
| [Get Datasource Stream Specs](actions/get-datasource-stream-specs.md) | GET |  |
| [Get Stream Contact](actions/get-stream-contact.md) | GET |  |
| [List Datasources](actions/list-datasources.md) | GET |  |
| [Push Stream Data](actions/push-stream-data.md) | POST |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Parameter Specs](actions/get-event-parameter-specs.md) | GET |  |
| [Get Project Event Specs](actions/get-project-event-specs.md) | GET |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS](actions/get-sms.md) | GET |  |
| [List SMS Senders](actions/list-sms-senders.md) | GET |  |
| [Send Direct SMS](actions/send-direct-sms.md) | POST |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Info](actions/get-project-info.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

