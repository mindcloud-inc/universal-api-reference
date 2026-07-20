# Bluebarry: Native API Reference

A consolidated summary of Bluebarry's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://data.bluebarry.ai/data
- **API base URL:** `https://data.bluebarry.ai/`

## Authentication

### API Key

Connect with a Bluebarry data API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://data.bluebarry.ai)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `$top` in the query string to set the page size (default 100; minimum 1). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contain`, `endswith`, `eq`, `gt`, `gte`, `lt`, `lte`, `ne`, `startswith`.

## Sorting

Set the sort field with `$orderby` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Advisor](actions/create-advisor.md) | `POST /data/Advisors` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Create Answer](actions/create-answer.md) | `POST /data/Answers` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Create Landing Page](actions/create-landing-page.md) | `POST /data/LandingPages` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Create Live Product Feed](actions/create-live-product-feed.md) | `POST /data/LiveProductFeeds` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Create Product](actions/create-product.md) | `POST /data/Products` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Create Question](actions/create-question.md) | `POST /data/Questions` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /data/WebhookSubscriptions` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Delete Advisor](actions/delete-advisor.md) | `DELETE /data/Advisors({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Delete Answer](actions/delete-answer.md) | `DELETE /data/Answers({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Delete Landing Page](actions/delete-landing-page.md) | `DELETE /data/LandingPages({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Delete Live Product Feed](actions/delete-live-product-feed.md) | `DELETE /data/LiveProductFeeds({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Delete Product](actions/delete-product.md) | `DELETE /data/Products({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Delete Question](actions/delete-question.md) | `DELETE /data/Questions({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /data/WebhookSubscriptions({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Get Advised Revenue Analytics](actions/get-advised-revenue-analytics.md) | `GET /data/GetAdvisedRevenueAnalytics(advisorId={advisorId},questionId={questionId},startDate={startDate},endDate={endDate})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Get Advisor](actions/get-advisor.md) | `GET /data/Advisors({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Get Answer](actions/get-answer.md) | `GET /data/Answers({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Get Average Session Duration](actions/get-average-session-duration.md) | `GET /data/GetAverageSessionDuration(advisorId={advisorId},questionId={questionId},startDate={startDate},endDate={endDate})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Get Completion Rate](actions/get-completion-rate.md) | `GET /data/GetCompletionRate(advisorId={advisorId},questionId={questionId},startDate={startDate},endDate={endDate})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Get Conversion Rate](actions/get-conversion-rate.md) | `GET /data/GetConversionRate(advisorId={advisorId},questionId={questionId},startDate={startDate},endDate={endDate})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Get Engagement Rate](actions/get-engagement-rate.md) | `GET /data/GetEngagementRate(advisorId={advisorId},questionId={questionId},startDate={startDate},endDate={endDate})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Get Landing Page](actions/get-landing-page.md) | `GET /data/LandingPages({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Get Live Product Feed](actions/get-live-product-feed.md) | `GET /data/LiveProductFeeds({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Get Product](actions/get-product.md) | `GET /data/Products({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Get Question](actions/get-question.md) | `GET /data/Questions({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | `GET /data/WebhookSubscriptions({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [List Advisors](actions/list-advisors.md) | `GET /data/Advisors` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [List Answers](actions/list-answers.md) | `GET /data/Answers` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [List Landing Pages](actions/list-landing-pages.md) | `GET /data/LandingPages` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [List Live Product Feeds](actions/list-live-product-feeds.md) | `GET /data/LiveProductFeeds` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [List Products](actions/list-products.md) | `GET /data/Products` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [List Questions](actions/list-questions.md) | `GET /data/Questions` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [List Settings](actions/list-settings.md) | `GET /data/Settings` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /data/WebhookSubscriptions` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Update Advisor](actions/update-advisor.md) | `PATCH /data/Advisors({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Update Answer](actions/update-answer.md) | `PATCH /data/Answers({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Update Landing Page](actions/update-landing-page.md) | `PATCH /data/LandingPages({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Update Live Product Feed](actions/update-live-product-feed.md) | `PATCH /data/LiveProductFeeds({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Update Product](actions/update-product.md) | `PATCH /data/Products({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Update Question](actions/update-question.md) | `PATCH /data/Questions({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
| [Update Webhook Subscription](actions/update-webhook-subscription.md) | `PATCH /data/WebhookSubscriptions({id})` | [docs](https://data.bluebarry.ai/data/$metadata) |
