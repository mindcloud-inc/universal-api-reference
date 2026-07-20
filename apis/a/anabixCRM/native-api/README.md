# Anabix CRM: Native API Reference

A consolidated summary of Anabix CRM's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf
- **API base URL:** `https://app.anabix.cz`

## Authentication

### Username and API Token

Use an Anabix username and API token from Nastroje - Hlavni nastaveni.

### Credentials

- **Username:** `username` · required · Anabix API username from Nastroje - Hlavni nastaveni.
- **API Token:** `token` · required · Anabix API token from Nastroje - Hlavni nastaveni.

[Official authentication documentation](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `data.limit` in the request body to set the page size (default 100; accepted range 1–200). Use `data.offset` in the request body as the record offset; numbering starts at 0.

## Filtering

Send filters in the request body.

## Sorting

Set the sort field with `data.orderBy` in the request body. Use `ASC` for ascending order and `DESC` for descending order. Multiple sort fields can be combined.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Create Contact](actions/create-contact.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Create Deal](actions/create-deal.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Create List](actions/create-list.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Create Organization](actions/create-organization.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Create Task](actions/create-task.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Get Activity](actions/get-activity.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Get Contact](actions/get-contact.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Get Deal](actions/get-deal.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Get List](actions/get-list.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Get Organization](actions/get-organization.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Get Task](actions/get-task.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [List Active Users](actions/list-active-users.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [List Activities](actions/list-activities.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [List Contacts](actions/list-contacts.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [List Deals](actions/list-deals.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [List Lists](actions/list-lists.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [List Organizations](actions/list-organizations.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [List Tasks](actions/list-tasks.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Manage Contact Lists](actions/manage-contact-lists.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Update Activity](actions/update-activity.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Update Contact](actions/update-contact.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Update Deal](actions/update-deal.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Update Organization](actions/update-organization.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
| [Update Task](actions/update-task.md) | `POST /api` | [docs](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf) |
