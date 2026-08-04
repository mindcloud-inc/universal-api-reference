# <img src="https://images.mindcloud.co/apps/icons/autotask_1784569363832.png" alt="Autotask logo" width="28" height="28"> Autotask: Universal API

Autotask: Manage companies, opportunities, projects, contacts, resources, and attachments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/autotask/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.kaseya.com/products/
- **Vendor API docs:** https://www.autotask.net/help/developerhelp/Content/APIs/REST/REST_API_Home.htm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Connection](actions/test-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autotask/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Count Opportunities](actions/count-opportunities.md) | GET |  |
| [Create Opportunity](actions/create-opportunity.md) | POST |  |
| [Get Opportunity](actions/get-opportunity.md) | GET |  |
| [List Opportunities](actions/list-opportunities.md) | GET |  |
| [Update Opportunity](actions/update-opportunity.md) | PUT |  |

### Opportunity Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity Attachment](actions/create-opportunity-attachment.md) | POST |  |
| [Get Opportunity Attachment](actions/get-opportunity-attachment.md) | GET |  |
| [List Opportunity Attachments](actions/list-opportunity-attachments.md) | GET |  |

### Opportunity Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Opportunity Category](actions/get-opportunity-category.md) | GET |  |
| [List Opportunity Categories](actions/list-opportunity-categories.md) | GET |  |

### Opportunity Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Opportunity Fields](actions/get-opportunity-fields.md) | GET |  |

### Opportunity User-defined Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Opportunity User-Defined Fields](actions/get-opportunity-user-defined-fields.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Count Projects](actions/count-projects.md) | GET |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Project Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Attachment](actions/get-project-attachment.md) | GET |  |
| [List Project Attachments](actions/list-project-attachments.md) | GET |  |

### Project Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Fields](actions/get-project-fields.md) | GET |  |

### Project User-defined Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Project User-Defined Fields](actions/get-project-user-defined-fields.md) | GET |  |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [List Resources](actions/list-resources.md) | GET |  |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [Test Connection](actions/test-connection.md) | GET |  |

