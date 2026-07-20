# Klenty: Native API Reference

A consolidated summary of Klenty's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://support.klenty.com/en/collections/5599717-webhooks-apis
- **API base URL:** `https://api.klenty.com/apis/v1/user/{username}`

## Authentication

### API Key

Connect with a Klenty API key and account email.

### Credentials

- **API Key:** `apiKey` · required
- **Username:** `username` · required · Enter the Klenty account email used in API request URLs.

Send these headers with each API request:

```http
x-API-key: <apiKey>
```

[Official authentication documentation](https://support.klenty.com/en/articles/3197537-getting-started-with-klenty-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (maximum 1000). Use `start` in the query string to choose the page; numbering starts at 1.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Prospect Custom Field Value](actions/add-prospect-custom-field-value.md) | `POST /prospects` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_fa068477d0) |
| [Add Prospect To List](actions/add-prospect-to-list.md) | `POST /prospects` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_8848b48485) |
| [Add Tags To Prospect](actions/add-tags-to-prospect.md) | `POST /prospects` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_8ab1e33aa8) |
| [Add Webhook](actions/add-webhook.md) | `POST /zapier/hooks` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_45a9638c98) |
| [Bulk Create Prospects](actions/bulk-create-prospects.md) | `POST /prospects` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_0356ba7595) |
| [Change Prospect To Do Not Contact](actions/change-prospect-to-do-not-contact.md) | `POST /prospects/:email/changeStatusToDoNotContact` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_99a462c518) |
| [Create Prospect](actions/create-prospect.md) | `POST /prospects` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_17d72e781c) |
| [Delete Webhook](actions/delete-webhook.md) | `POST /webhook/delete` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_ef5aaf283e) |
| [Get Call Completion Details](actions/get-call-completion-details.md) | `GET /calls` | [docs](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_b505b443a1) |
| [Get Email Engagements](actions/get-email-engagements.md) | `POST /emailEngagements` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_26cb69cafc) |
| [Get Prospect By Email](actions/get-prospect-by-email.md) | `GET /prospects` | [docs](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_b03c6d8d4d) |
| [Get Prospect Status By Email](actions/get-prospect-status-by-email.md) | `GET /prospects/{{email}}/status` | [docs](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_82c37984ec) |
| [Get Prospect Status By ID](actions/get-prospect-status-by-id.md) | `GET /prospects/{{id}}/status` | [docs](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_3e316f9dcc) |
| [Get Prospect With Custom Fields](actions/get-prospect-with-custom-fields.md) | `GET /prospects` | [docs](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_08b0294b78) |
| [Get Stepwise Metric Engagements](actions/get-stepwise-metric-engagements.md) | `POST /stepWiseEngagements` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_52fc68a546) |
| [List Company Cadences](actions/list-company-cadences.md) | `GET /cadences` | [docs](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_2256ed3433) |
| [List Lists](actions/list-lists.md) | `GET /lists` | [docs](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_c35a8af900) |
| [List Prospects By Created Date](actions/list-prospects-by-created-date.md) | `GET /prospects` | [docs](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_e9d493f674) |
| [List Prospects By Last Updated Date](actions/list-prospects-by-last-updated-date.md) | `GET /prospects` | [docs](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_b8930ef4b8) |
| [List Prospects By List](actions/list-prospects-by-list.md) | `GET /prospects` | [docs](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_82aa5a533c) |
| [List User Cadences](actions/list-user-cadences.md) | `GET /cadences` | [docs](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_80a1c4f4b5) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhook/getall` | [docs](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_d11c1fa847) |
| [Remove Tags From Prospect](actions/remove-tags-from-prospect.md) | `POST /prospects/:email/removeTags` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_4a906927ed) |
| [Resume Cadence](actions/resume-cadence.md) | `POST /cadences/resume` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_e44dfcb398) |
| [Revert Prospect From Do Not Contact](actions/revert-prospect-from-do-not-contact.md) | `POST /prospects/:email/revertStatusToDoNotContact` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_849206f8a2) |
| [Start Cadence](actions/start-cadence.md) | `POST /startcadence` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_c4b3f24c10) |
| [Stop Cadence For Prospect](actions/stop-cadence-for-prospect.md) | `POST /stopcadence` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_a2e9edeb59) |
| [Stop Prospect Mails](actions/stop-prospect-mails.md) | `POST /prospects/:email/stop` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_47985d38d5) |
| [Unsubscribe Prospect](actions/unsubscribe-prospect.md) | `POST /prospects/:email/unsubscribe` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_7860116467) |
| [Update Prospect](actions/update-prospect.md) | `POST /prospects/:email` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_3315dd4ccc) |
| [Update Webhook](actions/update-webhook.md) | `POST /webhook/update` | [docs](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_c5f05d6ef7) |
