# Thinkific: Native API Reference

A consolidated summary of Thinkific's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.thinkific.com/api/api-documentation
- **API base URL:** `https://api.thinkific.com/api/public/v1`

## Authentication

### API Key

### Credentials

- **API key:** `apiKey` · required
- **Subdomain:** `subdomain` · required · Your Thinkific site subdomain, for example myschool in myschool.thinkific.com.

Send these headers with each API request:

```http
X-Auth-API-Key: <apiKey>
X-Auth-Subdomain: <subdomain>
```

[Official authentication documentation](https://support.thinkific.dev/hc/en-us/articles/4422657425431-Authorization-using-API-Key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud Integration` |

Responses from this API use JSON. Response data is read from `items`. The total page count is read from `meta.pagination.total_pages`. The current page number is read from `meta.pagination.current_page`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–250). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Course Review](actions/create-course-review.md) | `POST /course_reviews` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1course_reviews/post) |
| [Create Enrollment](actions/create-enrollment.md) | `POST /enrollments` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1enrollments/post) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1groups/post) |
| [Create Instructor](actions/create-instructor.md) | `POST /instructors` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1instructors/post) |
| [Create Site Script](actions/create-site-script.md) | `POST /site_scripts` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1site_scripts/post) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1users/post) |
| [Get Course](actions/get-course.md) | `GET /courses/:id` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1courses~1{id}/get) |
| [Get Enrollment](actions/get-enrollment.md) | `GET /enrollments/:id` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1enrollments~1{id}/get) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1groups~1{id}/get) |
| [Get Instructor](actions/get-instructor.md) | `GET /instructors/:id` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1instructors~1{id}/get) |
| [Get Order](actions/get-order.md) | `GET /orders/:id` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1orders~1{id}/get) |
| [Get Product](actions/get-product.md) | `GET /products/:id` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1products~1{id}/get) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1users~1{id}/get) |
| [List Course Reviews](actions/list-course-reviews.md) | `GET /course_reviews` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1course_reviews/get) |
| [List Courses](actions/list-courses.md) | `GET /courses` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1courses/get) |
| [List Enrollments](actions/list-enrollments.md) | `GET /enrollments` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1enrollments/get) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1groups/get) |
| [List Instructors](actions/list-instructors.md) | `GET /instructors` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1instructors/get) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1orders/get) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1products/get) |
| [List Site Scripts](actions/list-site-scripts.md) | `GET /site_scripts` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1site_scripts/get) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1users/get) |
| [Update Enrollment](actions/update-enrollment.md) | `PUT /enrollments/:id` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1enrollments~1{id}/put) |
| [Update User](actions/update-user.md) | `PUT /users/:id` | [docs](https://developers.thinkific.com/api/api-documentation#/paths/~1users~1{id}/put) |
