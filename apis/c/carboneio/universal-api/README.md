# <img src="https://images.mindcloud.co/apps/icons/carboneio_1774893636613.png" alt="Carbone.io logo" width="28" height="28"> Carbone.io: Universal API

Generate and convert documents from templates, manage template assets, and retrieve rendered outputs through the Carbone Cloud API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/carboneio/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://carbone.io
- **Vendor API docs:** https://carbone.io/documentation/developer/http-api/introduction.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Convert Document](actions/convert-document.md) | POST | Creates a converted document from uploaded templates in Carbone.io. |
| [Generate Document](actions/generate-document.md) | POST | Creates a document from a stored Carbone.io template. |
| [Retrieve Generated Document](actions/retrieve-generated-document.md) | GET | Downloads a generated document from Carbone.io. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Status](actions/get-status.md) | GET | Retrieves service status from Carbone.io. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes a template from Carbone.io. |
| [Download Template](actions/download-template.md) | GET | Downloads a template from Carbone.io. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Carbone.io. |
| [Update Template](actions/update-template.md) | PUT | Updates a template in Carbone.io. |
| [Upload Template](actions/upload-template.md) | POST | Creates a template in Carbone.io. |

### Template Category

| Action | Method | Description |
| --- | --- | --- |
| [List Template Categories](actions/list-template-categories.md) | GET | Retrieves template categories from Carbone.io. |

### Template Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Template Tags](actions/list-template-tags.md) | GET | Retrieves template tags from Carbone.io. |

