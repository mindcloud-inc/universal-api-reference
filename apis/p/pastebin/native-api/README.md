# Pastebin: Native API Reference

A consolidated summary of Pastebin's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://pastebin.com/doc_api
- **API base URL:** `https://pastebin.com/api`

## Authentication

### Developer API key with optional user key

Connect with your Pastebin developer API key. Add a user key only for member-only endpoints.

### Credentials

- **Developer API key:** `apiDevKey` · required · Pastebin developer API key.
- **Optional user key:** `apiUserKey` · optional · Pastebin member user key from the API login flow. Only required for member-only endpoints.

[Official authentication documentation](https://pastebin.com/doc_api)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use plain text.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Guest Paste](actions/create-guest-paste.md) | `POST /api_post.php` | [docs](https://pastebin.com/doc_api) |
| [Create Member Paste](actions/create-member-paste.md) | `POST /api_post.php` | [docs](https://pastebin.com/doc_api) |
| [Create Paste In Folder](actions/create-paste-in-folder.md) | `POST /api_post.php` | [docs](https://pastebin.com/doc_api) |
| [Create Private Paste](actions/create-private-paste.md) | `POST /api_post.php` | [docs](https://pastebin.com/doc_api) |
| [Delete My Paste](actions/delete-my-paste.md) | `POST /api_post.php` | [docs](https://pastebin.com/doc_api) |
| [Generate User Session Key](actions/generate-user-session-key.md) | `POST /api_login.php` | [docs](https://pastebin.com/doc_api) |
| [Get Current User Details](actions/get-current-user-details.md) | `POST /api_post.php` | [docs](https://pastebin.com/doc_api) |
| [Get My Paste Raw Content](actions/get-my-paste-raw-content.md) | `POST https://pastebin.com/api/api_raw.php` | [docs](https://pastebin.com/doc_api) |
| [Get Raw Public Or Unlisted Paste](actions/get-raw-public-or-unlisted-paste.md) | `GET https://pastebin.com/raw/:pasteKey` | [docs](https://pastebin.com/doc_api) |
| [Get Scraped Paste Metadata](actions/get-scraped-paste-metadata.md) | `GET https://scrape.pastebin.com/api_scrape_item_meta.php` | [docs](https://pastebin.com/doc_scraping_api) |
| [Get Scraped Paste Raw Data](actions/get-scraped-paste-raw-data.md) | `GET https://scrape.pastebin.com/api_scrape_item.php` | [docs](https://pastebin.com/doc_scraping_api) |
| [List My Pastes](actions/list-my-pastes.md) | `POST /api_post.php` | [docs](https://pastebin.com/doc_api) |
| [List Recent Public Pastes](actions/list-recent-public-pastes.md) | `GET https://scrape.pastebin.com/api_scraping.php` | [docs](https://pastebin.com/doc_scraping_api) |
