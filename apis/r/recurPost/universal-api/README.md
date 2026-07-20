# <img src="https://images.mindcloud.co/apps/icons/recur-post_1775847688057.png" alt="RecurPost logo" width="28" height="28"> RecurPost: Universal API

Connect profiles, manage libraries, schedule posts, and generate content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/recurPost/latest
- **Category:** Marketing / Social Media
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://recurpost.com/
- **Vendor API docs:** https://developers.recurpost.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [User Login](actions/user-login.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/user-login?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Ai Content

| Action | Method | Description |
| --- | --- | --- |
| [Generate Content with AI](actions/generate-content-with-ai.md) | POST | Generates social content with AI in RecurPost. |

### Generated Image

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image with AI](actions/generate-image-with-ai.md) | POST | Generates an image with AI in RecurPost. |

### Library

| Action | Method | Description |
| --- | --- | --- |
| [List Libraries](actions/list-libraries.md) | GET | Retrieves content libraries from RecurPost. |

### Library Content

| Action | Method | Description |
| --- | --- | --- |
| [Add Content to Library](actions/add-content-to-library.md) | POST | Creates library content in RecurPost. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Post Content](actions/post-content.md) | POST | Creates a social post in RecurPost. |

### Post History Record

| Action | Method | Description |
| --- | --- | --- |
| [List Post History](actions/list-post-history.md) | GET | Retrieves post history from RecurPost by social account. |

### Social Account

| Action | Method | Description |
| --- | --- | --- |
| [List Social Accounts](actions/list-social-accounts.md) | GET | Retrieves social accounts from RecurPost. |

### Social Account Connection Url

| Action | Method | Description |
| --- | --- | --- |
| [Connect Social Account URLs](actions/connect-social-account-urls.md) | GET | Retrieves social account connection URLs from RecurPost. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [User Login](actions/user-login.md) | GET | Verifies RecurPost API credentials. |

