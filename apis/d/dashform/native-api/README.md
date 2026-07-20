# Dashform: Native API Reference

A consolidated summary of Dashform's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://github.com/makloai/dashform-cli-docs
- **API base URL:** `https://getaiform.com`

## Authentication

### Dashform API Key

Create an API key in Dashform under Account -> API Keys, then paste it here. Dashform sends it as the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://getaiform.com/dashboard/account/api-keys)

## API conventions

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | `POST /api/v1/forms` | [docs](https://github.com/makloai/dashform-cli-docs#forms-create) |
| [Delete Form](actions/delete-form.md) | `DELETE /api/v1/forms/:id` | [docs](https://github.com/makloai/dashform-cli-docs#forms-delete) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v1/me` | [docs](https://github.com/makloai/dashform-cli-docs#auth-whoami) |
| [Get Form](actions/get-form.md) | `GET /api/v1/forms/:id` | [docs](https://github.com/makloai/dashform-cli-docs#forms-get) |
| [List Forms](actions/list-forms.md) | `GET /api/v1/forms` | [docs](https://github.com/makloai/dashform-cli-docs#forms-list) |
| [Update Form](actions/update-form.md) | `PATCH /api/v1/forms/:id` | [docs](https://github.com/makloai/dashform-cli-docs#forms-update) |
