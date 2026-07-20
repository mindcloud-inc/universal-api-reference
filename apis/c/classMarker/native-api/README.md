# ClassMarker: Native API Reference

A consolidated summary of ClassMarker's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://www.classmarker.com/online-testing/docs/api/
- **API base URL:** `https://api.classmarker.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `apiSecret` · required · ClassMarker API secret paired with your API key.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.classmarker.com/online-testing/docs/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 200; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Access Codes](actions/add-access-codes.md) | `POST /v1/accesslists/{access_list_id}.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#post-access-codes) |
| [Create Category](actions/create-category.md) | `POST /v1/categories/category.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#post-category) |
| [Create Parent Category](actions/create-parent-category.md) | `POST /v1/categories/parent_category.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#post-parent-category) |
| [Create Question](actions/create-question.md) | `POST /v1/questions.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#post-question) |
| [Get Question](actions/get-question.md) | `GET /v1/questions/{question_id}.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#get-question) |
| [List Available Groups Links and Exams](actions/list-available-groups-links-and-exams.md) | `GET /v1.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#get-all-available-groups-links-and-exams) |
| [List Categories](actions/list-categories.md) | `GET /v1/categories.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#get-all-categories) |
| [List Questions](actions/list-questions.md) | `GET /v1/questions.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#get-all-questions-in-your-question-bank) |
| [List Recent Results for All Groups](actions/list-recent-results-for-all-groups.md) | `GET /v1/groups/recent_results.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#get-recent-results-for-all-groups) |
| [List Recent Results for All Links](actions/list-recent-results-for-all-links.md) | `GET /v1/links/recent_results.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#get-recent-results-for-all-links) |
| [List Recent Results for Specific Group Exam](actions/list-recent-results-for-specific-group-exam.md) | `GET /v1/groups/{group_id}/tests/{test_id}/recent_results.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#get-recent-results-for-specific-group-exam) |
| [List Recent Results for Specific Link Exam](actions/list-recent-results-for-specific-link-exam.md) | `GET /v1/links/{link_id}/tests/{test_id}/recent_results.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#get-recent-results-for-specific-link-exam) |
| [Remove Access Codes](actions/remove-access-codes.md) | `DELETE /v1/accesslists/{access_list_id}.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#delete-access-codes) |
| [Update Category](actions/update-category.md) | `PUT /v1/category/{category_id}.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#put-category) |
| [Update Parent Category](actions/update-parent-category.md) | `PUT /v1/categories/parent_category/{parent_category_id}.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#put-parent-category) |
| [Update Question](actions/update-question.md) | `PUT /v1/questions/{question_id}.json` | [docs](https://www.classmarker.com/online-testing/docs/api/#put-question) |
