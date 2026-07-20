# Meegle: Native API Reference

A consolidated summary of Meegle's API configuration, with links to official documentation.

- **Official docs:** https://www.meegle.com/b/helpcenter/developer
- **API base URL:** `https://www.meegle.com`

## Authentication

### Meegle Custom Auth

Custom Meegle plugin-token authentication using Plugin ID, Plugin Secret, and User Key.

### Credentials

- **Plugin ID:** `plugin_id` · required
- **Plugin Secret:** `plugin_secret` · required · Meegle plugin secret used to mint plugin_access_token.
- **User Key:** `user_key` · required · Meegle user_key for user-scoped request flows when required.

[Official authentication documentation](https://www.meegle.com/b/helpcenter/developer/plugin-access-token-obtain-a-plugin-access-token#8f4c51ff)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
