# Instafill: Native API Reference

A consolidated summary of Instafill's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://docs.instafill.ai/docs/api/intro
- **OpenAPI specification:** https://api.instafill.ai/swagger/v1/swagger.json
- **API base URL:** `https://api.instafill.ai`

## Authentication

### API Key

Authenticate requests with Authorization: Bearer <your Instafill API key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.instafill.ai/docs/api/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Flat PDF](actions/check-flat.md) | `POST /v1/utils/check-flat` | [docs](https://docs.instafill.ai/docs/api/utils/check-flat) |
| [Convert Form](actions/convert-form.md) | `POST /v1/utils/convert` | [docs](https://docs.instafill.ai/docs/api/utils/convert-form) |
| [Create Profile](actions/create-profile.md) | `POST /v1/profiles` | [docs](https://api.instafill.ai/swagger) |
| [Create Session](actions/create-session.md) | `POST /v1/sessions` | [docs](https://docs.instafill.ai/docs/api/sessions/create-session) |
| [Delete Make Hook](actions/delete-make-hook.md) | `DELETE /v1/integrations/make/hooks/:id` | [docs](https://api.instafill.ai/swagger) |
| [Delete n8n Hook](actions/delete-n8n-hook.md) | `DELETE /v1/integrations/n8n/hooks/:id` | [docs](https://api.instafill.ai/swagger) |
| [Delete Power Automate Hook](actions/delete-power-automate-hook.md) | `DELETE /v1/integrations/power-automate/hooks/:id` | [docs](https://api.instafill.ai/swagger) |
| [Delete Profile](actions/delete-profile.md) | `DELETE /v1/profiles/:profileId` | [docs](https://api.instafill.ai/swagger) |
| [Delete Profile File](actions/delete-profile-file.md) | `DELETE /v1/profiles/:profileId/files/:fileId` | [docs](https://api.instafill.ai/swagger) |
| [Delete Zapier Hook](actions/delete-zapier-hook.md) | `DELETE /v1/integrations/zapier/hooks/:id` | [docs](https://docs.instafill.ai/docs/integrations/zapier) |
| [Get Account Details](actions/get-account-details.md) | `GET /v1/account/me` | [docs](https://api.instafill.ai/swagger) |
| [Get Conversion Status](actions/get-conversion-status.md) | `GET /v1/utils/convert/:jobId/status` | [docs](https://docs.instafill.ai/docs/api/utils/convert-status) |
| [Get Form](actions/get-form.md) | `GET /v1/forms/:id` | [docs](https://docs.instafill.ai/docs/api/forms/get-form) |
| [Get Profile](actions/get-profile.md) | `GET /v1/profiles/:profileId` | [docs](https://api.instafill.ai/swagger) |
| [Get Session](actions/get-session.md) | `GET /v1/sessions/:id` | [docs](https://docs.instafill.ai/docs/api/sessions/get-session) |
| [Get Zapier Hook Sample](actions/get-zapier-hook-sample.md) | `GET /v1/integrations/zapier/hooks/sample` | [docs](https://docs.instafill.ai/docs/integrations/zapier) |
| [List Forms](actions/list-forms.md) | `GET /v1/forms` | [docs](https://docs.instafill.ai/docs/api/forms/list-forms) |
| [List Profiles](actions/list-profiles.md) | `GET /v1/profiles` | [docs](https://api.instafill.ai/swagger) |
| [List Sessions](actions/list-sessions.md) | `GET /v1/sessions` | [docs](https://api.instafill.ai/swagger) |
| [Search Forms](actions/search-forms.md) | `GET /v1/forms/search` | [docs](https://api.instafill.ai/swagger) |
| [Subscribe Make Hook](actions/subscribe-make-hook.md) | `POST /v1/integrations/make/hooks/subscribe` | [docs](https://api.instafill.ai/swagger) |
| [Subscribe n8n Hook](actions/subscribe-n8n-hook.md) | `POST /v1/integrations/n8n/hooks/subscribe` | [docs](https://api.instafill.ai/swagger) |
| [Subscribe Power Automate Hook](actions/subscribe-power-automate-hook.md) | `POST /v1/integrations/power-automate/hooks/subscribe` | [docs](https://api.instafill.ai/swagger) |
| [Subscribe Zapier Hook](actions/subscribe-zapier-hook.md) | `POST /v1/integrations/zapier/hooks/subscribe` | [docs](https://docs.instafill.ai/docs/integrations/zapier) |
| [Update Profile Name](actions/update-profile-name.md) | `PATCH /v1/profiles/:profileId/name` | [docs](https://api.instafill.ai/swagger) |
| [Update Profile Text Info](actions/update-profile-text-info.md) | `PUT /v1/profiles/:profileId` | [docs](https://api.instafill.ai/swagger) |
| [Upload Form](actions/upload-form.md) | `POST /v1/forms/upload` | [docs](https://docs.instafill.ai/docs/api/forms/create-a-form) |
| [Upload Profile File](actions/upload-profile-file.md) | `POST /v1/profiles/:profileId/files` | [docs](https://api.instafill.ai/swagger) |
