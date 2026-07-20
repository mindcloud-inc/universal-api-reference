# RecurPost: Native API Reference

A consolidated summary of RecurPost's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://developers.recurpost.com/
- **API base URL:** `https://social.recurpost.com`

## Authentication

### API Key

Use your RecurPost account email and API pass key.

### Credentials

- **API Key:** `apiKey` · required
- **Email:** `emailId` · required · Email id of the RecurPost account used for API requests.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.recurpost.com/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Content to Library](actions/add-content-to-library.md) | `POST /api/add_content_in_library` | [docs](https://developers.recurpost.com/) |
| [Connect Social Account URLs](actions/connect-social-account-urls.md) | `POST /api/connect_social_account_urls` | [docs](https://developers.recurpost.com/) |
| [Generate Content with AI](actions/generate-content-with-ai.md) | `POST /api/generate_content_with_ai` | [docs](https://developers.recurpost.com/) |
| [Generate Image with AI](actions/generate-image-with-ai.md) | `POST /api/generate_image_with_ai` | [docs](https://developers.recurpost.com/) |
| [List Libraries](actions/list-libraries.md) | `POST /api/library_list` | [docs](https://developers.recurpost.com/) |
| [List Post History](actions/list-post-history.md) | `POST /api/history_data` | [docs](https://developers.recurpost.com/) |
| [List Social Accounts](actions/list-social-accounts.md) | `POST /api/social_account_list` | [docs](https://developers.recurpost.com/) |
| [Post Content](actions/post-content.md) | `POST /api/post_content` | [docs](https://developers.recurpost.com/) |
| [User Login](actions/user-login.md) | `POST /api/user_login` | [docs](https://developers.recurpost.com/) |
