# <img src="https://images.mindcloud.co/apps/icons/bluebarry_1774972420887.png" alt="Bluebarry logo" width="28" height="28"> Bluebarry: Universal API

Build quiz funnels, landing pages, product feeds, and recommendations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bluebarry/latest
- **Category:** Commerce
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bluebarry.ai
- **Vendor API docs:** https://data.bluebarry.ai/data

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Advisors](actions/list-advisors.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-advisors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Advisor

| Action | Method | Description |
| --- | --- | --- |
| [Create Advisor](actions/create-advisor.md) | POST | Creates a new advisor in Bluebarry. |
| [Delete Advisor](actions/delete-advisor.md) | DELETE | Deletes an existing advisor from Bluebarry. |
| [Get Advisor](actions/get-advisor.md) | GET | Retrieves a single advisor from Bluebarry. |
| [List Advisors](actions/list-advisors.md) | GET | Retrieves advisor entity records from Bluebarry. |
| [Update Advisor](actions/update-advisor.md) | PUT | Updates an existing advisor in Bluebarry. |

### Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Advised Revenue Analytics](actions/get-advised-revenue-analytics.md) | GET | Retrieves advised revenue analytics from Bluebarry. |
| [Get Average Session Duration](actions/get-average-session-duration.md) | GET | Retrieves average session duration analytics from Bluebarry. |
| [Get Completion Rate](actions/get-completion-rate.md) | GET | Retrieves completion rate analytics from Bluebarry. |
| [Get Conversion Rate](actions/get-conversion-rate.md) | GET | Retrieves conversion rate analytics from Bluebarry. |
| [Get Engagement Rate](actions/get-engagement-rate.md) | GET | Retrieves engagement rate analytics from Bluebarry. |

### Answer

| Action | Method | Description |
| --- | --- | --- |
| [Create Answer](actions/create-answer.md) | POST | Creates a new answer in Bluebarry. |
| [Delete Answer](actions/delete-answer.md) | DELETE | Deletes an existing answer from Bluebarry. |
| [Get Answer](actions/get-answer.md) | GET | Retrieves a single answer from Bluebarry. |
| [List Answers](actions/list-answers.md) | GET | Retrieves answer entity records from Bluebarry. |
| [Update Answer](actions/update-answer.md) | PUT | Updates an existing answer in Bluebarry. |

### Landingpage

| Action | Method | Description |
| --- | --- | --- |
| [Create Landing Page](actions/create-landing-page.md) | POST | Creates a new landing page in Bluebarry. |
| [Delete Landing Page](actions/delete-landing-page.md) | DELETE | Deletes a landing page from Bluebarry. |
| [Get Landing Page](actions/get-landing-page.md) | GET | Retrieves a landing page from Bluebarry. |
| [List Landing Pages](actions/list-landing-pages.md) | GET | Retrieves landing page records from Bluebarry. |
| [Update Landing Page](actions/update-landing-page.md) | PUT | Updates an existing landing page in Bluebarry. |

### Liveproductfeed

| Action | Method | Description |
| --- | --- | --- |
| [Create Live Product Feed](actions/create-live-product-feed.md) | POST | Creates a new live product feed in Bluebarry. |
| [Delete Live Product Feed](actions/delete-live-product-feed.md) | DELETE | Deletes a live product feed from Bluebarry. |
| [Get Live Product Feed](actions/get-live-product-feed.md) | GET | Retrieves a live product feed from Bluebarry. |
| [List Live Product Feeds](actions/list-live-product-feeds.md) | GET | Retrieves live product feeds from Bluebarry. |
| [Update Live Product Feed](actions/update-live-product-feed.md) | PUT | Updates an existing live product feed in Bluebarry. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Bluebarry. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Bluebarry. |
| [Get Product](actions/get-product.md) | GET | Retrieves a single product from Bluebarry. |
| [List Products](actions/list-products.md) | GET | Retrieves product entity records from Bluebarry. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Bluebarry. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Create Question](actions/create-question.md) | POST | Creates a new question in Bluebarry. |
| [Delete Question](actions/delete-question.md) | DELETE | Deletes an existing question from Bluebarry. |
| [Get Question](actions/get-question.md) | GET | Retrieves a single question from Bluebarry. |
| [List Questions](actions/list-questions.md) | GET | Retrieves question entity records from Bluebarry. |
| [Update Question](actions/update-question.md) | PUT | Updates an existing question in Bluebarry. |

### Setting

| Action | Method | Description |
| --- | --- | --- |
| [List Settings](actions/list-settings.md) | GET | Retrieves settings entity records from Bluebarry. |

### Webhooksubscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a new webhook subscription in Bluebarry. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes a webhook subscription from Bluebarry. |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | GET | Retrieves a webhook subscription from Bluebarry. |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves webhook subscription records from Bluebarry. |
| [Update Webhook Subscription](actions/update-webhook-subscription.md) | PUT | Updates an existing webhook subscription in Bluebarry. |

