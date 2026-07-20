# ProvenExpert: Native API Reference

A consolidated summary of ProvenExpert's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developer.provenexpert.com/index_en.html
- **API base URL:** `https://www.provenexpert.com/api/v1`

## Authentication

### Basic

Authenticate with your ProvenExpert API ID and API key.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.provenexpert.com/index_en.html#authentication)

## API conventions

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Invitation Link](actions/create-invitation-link.md) | `POST /invite/url/create` | [docs](https://developer.provenexpert.com/index_en.html#invite-url-create) |
| [Create Invitation Mail](actions/create-invitation-mail.md) | `POST /invite/mail/create` | [docs](https://developer.provenexpert.com/index_en.html#invite-mail-create) |
| [Create Profile](actions/create-profile.md) | `POST /profile/create` | [docs](https://developer.provenexpert.com/index_en.html#profile-create) |
| [Create Survey](actions/create-survey.md) | `POST /survey/create` | [docs](https://developer.provenexpert.com/index_en.html#survey-create) |
| [Create Widget](actions/create-widget.md) | `POST /widget/create` | [docs](https://developer.provenexpert.com/index_en.html#widget-create) |
| [Get API Credentials](actions/get-api-credentials.md) | `GET /auth/api/get` | [docs](https://developer.provenexpert.com/index_en.html#auth-api-get) |
| [Get Invitation Mail Status](actions/get-invitation-mail-status.md) | `POST /invite/mail/status` | [docs](https://developer.provenexpert.com/index_en.html#invite-mail-status) |
| [Get Login URL](actions/get-login-url.md) | `POST /auth/url/get` | [docs](https://developer.provenexpert.com/index_en.html#auth-url-get) |
| [Get Profile](actions/get-profile.md) | `POST /profile/get` | [docs](https://developer.provenexpert.com/index_en.html#profile-get) |
| [Get Profile Settings](actions/get-profile-settings.md) | `POST /profile/settings/get` | [docs](https://developer.provenexpert.com/index_en.html#profile-settings-get) |
| [Get Rating Summary](actions/get-rating-summary.md) | `POST /rating/summary/get` | [docs](https://developer.provenexpert.com/index_en.html#rating-summary-get) |
| [Get Rich Snippet](actions/get-rich-snippet.md) | `POST /rating/summary/richsnippet` | [docs](https://developer.provenexpert.com/index_en.html#rating-summary-richsnippet) |
| [List Child API Credentials](actions/list-child-api-credentials.md) | `GET /auth/api/children` | [docs](https://developer.provenexpert.com/index_en.html#auth-api-children) |
| [List Child Profiles](actions/list-child-profiles.md) | `GET /profile/children` | [docs](https://developer.provenexpert.com/index_en.html#profile-children) |
| [List Child Rating Summaries](actions/list-child-rating-summaries.md) | `GET /rating/summary/children` | [docs](https://developer.provenexpert.com/index_en.html#rating-summary-children) |
| [List Invitation Links](actions/list-invitation-links.md) | `POST /invite/url/get` | [docs](https://developer.provenexpert.com/index_en.html#invite-url-get) |
| [List Surveys](actions/list-surveys.md) | `POST /survey/get` | [docs](https://developer.provenexpert.com/index_en.html#survey-get) |
| [Update Profile](actions/update-profile.md) | `POST /profile/update` | [docs](https://developer.provenexpert.com/index_en.html#profile-update) |
| [Update Profile Settings](actions/update-profile-settings.md) | `POST /profile/settings/update` | [docs](https://developer.provenexpert.com/index_en.html#profile-settings-update) |
| [Update Survey](actions/update-survey.md) | `POST /survey/update` | [docs](https://developer.provenexpert.com/index_en.html#survey-update) |
