# <img src="https://images.mindcloud.co/apps/icons/prod-pad_1774463345006.png" alt="ProdPad logo" width="28" height="28"> ProdPad: Universal API

Manage product feedback, ideas, and roadmaps

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/prodPad/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.prodpad.com
- **Vendor API docs:** https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Ideas](actions/list-ideas.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-ideas?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in ProdPad. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from ProdPad. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from ProdPad. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in ProdPad. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in ProdPad. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from ProdPad. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from ProdPad. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in ProdPad. |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Create Feedback](actions/create-feedback.md) | POST | Creates new feedback in ProdPad. |
| [Get Feedback](actions/get-feedback.md) | GET | Retrieves feedback from ProdPad. |
| [List Feedback](actions/list-feedback.md) | GET | Retrieves feedback from ProdPad. |
| [Update Feedback](actions/update-feedback.md) | PUT | Updates existing feedback in ProdPad. |

### Idea

| Action | Method | Description |
| --- | --- | --- |
| [Create Idea](actions/create-idea.md) | POST | Creates a new idea in ProdPad. |
| [Get Idea](actions/get-idea.md) | GET | Retrieves an idea from ProdPad. |
| [List Ideas](actions/list-ideas.md) | GET | Retrieves ideas from ProdPad. |
| [Update Idea](actions/update-idea.md) | PUT | Updates an existing idea in ProdPad. |

### Objective

| Action | Method | Description |
| --- | --- | --- |
| [Create Objective](actions/create-objective.md) | POST | Creates a new objective in ProdPad. |
| [Get Objective](actions/get-objective.md) | GET | Retrieves an objective from ProdPad. |
| [List Objectives](actions/list-objectives.md) | GET | Retrieves objectives from ProdPad. |
| [Update Objective](actions/update-objective.md) | PUT | Updates an existing objective in ProdPad. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from ProdPad. |
| [List Products](actions/list-products.md) | GET | Retrieves products from ProdPad. |

### User Story

| Action | Method | Description |
| --- | --- | --- |
| [Create User Story](actions/create-user-story.md) | POST | Creates a new user story in ProdPad. |
| [List User Stories](actions/list-user-stories.md) | GET | Retrieves user stories from ProdPad. |

