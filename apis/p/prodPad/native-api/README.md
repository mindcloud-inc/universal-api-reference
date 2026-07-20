# ProdPad: Native API Reference

A consolidated summary of ProdPad's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4
- **OpenAPI specification:** https://api.swaggerhub.com/apis/ProdPad/prodpad/1.1.4
- **API base URL:** `https://api.prodpad.com/v1`

## Authentication

### API Key

Connect with a ProdPad API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.prodpad.com/article/763-generating-an-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `size` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/PostCompanies) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/PostContacts) |
| [Create Feedback](actions/create-feedback.md) | `POST /feedbacks` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/PostFeedbacks) |
| [Create Idea](actions/create-idea.md) | `POST /ideas` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Ideas/PostIdeas) |
| [Create Objective](actions/create-objective.md) | `POST /objectives` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Products/PostObjectives) |
| [Create User Story](actions/create-user-story.md) | `POST /userstories` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Ideas/PostUserStories) |
| [Get Company](actions/get-company.md) | `GET /companies/:id` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/GetCompany) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/GetContact) |
| [Get Feedback](actions/get-feedback.md) | `GET /feedbacks/:id` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/GetFeedback) |
| [Get Idea](actions/get-idea.md) | `GET /ideas/:id` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Ideas/GetIdeaByID) |
| [Get Objective](actions/get-objective.md) | `GET /objectives/:id` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Products/GetObjective) |
| [Get Product](actions/get-product.md) | `GET /products/:id` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Products/GetProduct) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/GetCompanies) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/GetContacts) |
| [List Feedback](actions/list-feedback.md) | `GET /feedbacks` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/GetFeedbacks) |
| [List Ideas](actions/list-ideas.md) | `GET /ideas` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Ideas/GetIdeas) |
| [List Objectives](actions/list-objectives.md) | `GET /objectives` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Products/GetObjectives) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Products/GetProducts) |
| [List User Stories](actions/list-user-stories.md) | `GET /userstories` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Ideas/GetUserStories) |
| [Update Company](actions/update-company.md) | `PUT /companies/:id` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/PutCompany) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/PutContact) |
| [Update Feedback](actions/update-feedback.md) | `PUT /feedbacks/:id` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/PutFeedback) |
| [Update Idea](actions/update-idea.md) | `PUT /ideas/:id` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Ideas/PutIdea) |
| [Update Objective](actions/update-objective.md) | `PUT /objectives/:id` | [docs](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Products/PutObjective) |
