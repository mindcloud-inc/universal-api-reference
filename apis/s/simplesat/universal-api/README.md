# <img src="https://images.mindcloud.co/apps/icons/simplesat_1773954509079.png" alt="Simplesat logo" width="28" height="28"> Simplesat: Universal API

Collect, send, and analyze customer feedback surveys

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/simplesat/latest
- **Category:** Support / Customer Success
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.simplesat.io
- **Vendor API docs:** https://developer.simplesat.io/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Surveys](actions/list-surveys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Answer

| Action | Method | Description |
| --- | --- | --- |
| [Get Answer](actions/get-answer.md) | GET | Retrieves an answer from Simplesat. |
| [Search Answers](actions/search-answers.md) | GET | Searches answers in Simplesat. |
| [Update Answer](actions/update-answer.md) | PUT | Updates an existing answer in Simplesat. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Upsert Customers](actions/bulk-upsert-customers.md) | POST | Creates or updates multiple customers in Simplesat. |
| [Create or Update Customer](actions/create-or-update-customer.md) | POST | Creates or updates a customer in Simplesat. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Simplesat. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Simplesat. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Simplesat. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [List Questions](actions/list-questions.md) | GET | Retrieves questions from Simplesat. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Response](actions/create-or-update-response.md) | POST | Creates or updates a response in Simplesat. |
| [Get Response](actions/get-response.md) | GET | Retrieves a response from Simplesat. |
| [Search Responses](actions/search-responses.md) | GET | Searches responses in Simplesat. |
| [Update Response](actions/update-response.md) | PUT | Updates an existing response in Simplesat. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves surveys from Simplesat. |

### Survey Email Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Survey by Email](actions/send-survey-by-email.md) | POST | Sends a survey by email from Simplesat. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Team Member](actions/create-or-update-team-member.md) | POST | Creates or updates a team member in Simplesat. |
| [Get Team Member](actions/get-team-member.md) | GET | Retrieves a team member from Simplesat. |

