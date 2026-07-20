# Jaicob: Native API Reference

A consolidated summary of Jaicob's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.jaicob.ai/reference
- **OpenAPI specification:** https://api.jaicob.ai/docs-json
- **API base URL:** `https://api.jaicob.ai`

## Authentication

### API Key

Connect Jaicob with an API key generated in Jaicob settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://developers.jaicob.ai/docs/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Pagination

Use `take` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Application](actions/create-application.md) | `POST /applications/[:vacancyId]` | [docs](https://developers.jaicob.ai/reference/create_application) |
| [Create Candidate](actions/create-candidate.md) | `POST /candidates` | [docs](https://developers.jaicob.ai/reference/create_candidate) |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://developers.jaicob.ai/reference/create_client) |
| [Create Location](actions/create-location.md) | `POST /locations` | [docs](https://developers.jaicob.ai/reference/create_location) |
| [Create Vacancy](actions/create-vacancy.md) | `POST /vacancies` | [docs](https://developers.jaicob.ai/reference/create_vacancy) |
| [List Applications](actions/list-applications.md) | `GET /applications/public` | [docs](https://developers.jaicob.ai/reference/list_applications) |
| [List Candidates](actions/list-candidates.md) | `GET /candidates/public` | [docs](https://developers.jaicob.ai/reference/list_candidates) |
| [List Clients](actions/list-clients.md) | `GET /clients/public` | [docs](https://developers.jaicob.ai/reference/list_clients) |
| [List Educations](actions/list-educations.md) | `GET /taxonomies/educations` | [docs](https://developers.jaicob.ai/reference/retrieve_educations) |
| [List Industries](actions/list-industries.md) | `GET /taxonomies/industries` | [docs](https://developers.jaicob.ai/reference/retrieve_industries) |
| [List Job Categories](actions/list-job-categories.md) | `GET /taxonomies/job-categories` | [docs](https://developers.jaicob.ai/reference/retrieve_job_categories) |
| [List Locations](actions/list-locations.md) | `GET /locations/public` | [docs](https://developers.jaicob.ai/reference/list_locations) |
| [List Seniorities](actions/list-seniorities.md) | `GET /taxonomies/seniorities` | [docs](https://developers.jaicob.ai/reference/retrieve_seniorities) |
| [List Vacancies](actions/list-vacancies.md) | `GET /vacancies/public` | [docs](https://developers.jaicob.ai/reference/list_vacancies) |
| [Parse Resume](actions/parse-resume.md) | `POST /file/resume` | [docs](https://developers.jaicob.ai/reference/parse_resume) |
| [Retrieve Application](actions/retrieve-application.md) | `GET /applications/public/[:id]` | [docs](https://developers.jaicob.ai/reference/retrieve_application) |
| [Retrieve Candidate](actions/retrieve-candidate.md) | `GET /candidates/public/[:id]` | [docs](https://developers.jaicob.ai/reference/retrieve_candidate) |
| [Retrieve Client](actions/retrieve-client.md) | `GET /clients/public/[:id]` | [docs](https://developers.jaicob.ai/reference/retrieve_client) |
| [Retrieve Location](actions/retrieve-location.md) | `GET /locations/public/[:id]` | [docs](https://developers.jaicob.ai/reference/retrieve_location) |
| [Retrieve Vacancy](actions/retrieve-vacancy.md) | `GET /vacancies/public/[:id]` | [docs](https://developers.jaicob.ai/reference/retrieve_vacancy) |
| [Update Candidate](actions/update-candidate.md) | `PUT /candidates/[:id]` | [docs](https://developers.jaicob.ai/reference/update_candidate) |
| [Update Client](actions/update-client.md) | `PUT /clients/[:id]` | [docs](https://developers.jaicob.ai/reference/update_client) |
| [Update Location](actions/update-location.md) | `PUT /locations/[:id]` | [docs](https://developers.jaicob.ai/reference/update_location) |
| [Update Vacancy](actions/update-vacancy.md) | `PUT /vacancies/[:id]` | [docs](https://developers.jaicob.ai/reference/update_vacancy) |
