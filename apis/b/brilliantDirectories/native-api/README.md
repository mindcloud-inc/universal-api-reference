# Brilliant Directories: Native API Reference

A consolidated summary of Brilliant Directories's API configuration, with links to official documentation.

- **Official docs:** https://support.brilliantdirectories.com/support/solutions/folders/12000019107
- **API base URL:** `https://launch60827.directoryup.com`

## Authentication

### Site API Key

Connect with your Brilliant Directories site base URL and API key. Requests are sent with the X-Api-Key header.

### Credentials

- **Site Base URL:** `siteBaseUrl` · required · The full base URL of your Brilliant Directories site, including https://.
- **API Key:** `apiKey` · required · Your Brilliant Directories API key, sent in the X-Api-Key request header.

[Official authentication documentation](https://support.brilliantdirectories.com/support/solutions/articles/12000103947-users-api-how-to-manage-users-with-api-calls)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.
