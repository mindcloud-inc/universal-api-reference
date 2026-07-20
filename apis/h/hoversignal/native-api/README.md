# Hoversignal: Native API Reference

A consolidated summary of Hoversignal's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://app.hoversignal.com/docs/ui/index
- **OpenAPI specification:** https://app.hoversignal.com/docs/v1
- **API base URL:** `https://app.hoversignal.com`

## Authentication

### API Key

Connect Hoversignal using an API key sent in the X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://hoversignal.com/how-to/integrations/api-documentation)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Easter Egg Hook](actions/create-easter-egg-hook.md) | `POST /api/v1/hooks/easterEgg` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Create Feedback Hook](actions/create-feedback-hook.md) | `POST /api/v1/hooks/feedback` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Create Form Hook](actions/create-form-hook.md) | `POST /api/v1/hooks/form` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Create Lottery Hook](actions/create-lottery-hook.md) | `POST /api/v1/hooks/lottery` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Create Quiz Hook](actions/create-quiz-hook.md) | `POST /api/v1/hooks/quiz` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Create Signal](actions/create-signal.md) | `POST /api/v1/signals` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Create Signal Hook](actions/create-signal-hook.md) | `POST /api/v1/hooks` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Create Spinner Hook](actions/create-spinner-hook.md) | `POST /api/v1/hooks/spinner` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Delete Easter Egg Hook](actions/delete-easter-egg-hook.md) | `DELETE /api/v1/hooks/easterEgg/{hookId}` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Delete Feedback Hook](actions/delete-feedback-hook.md) | `DELETE /api/v1/hooks/feedback/{hookId}` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Delete Form Hook](actions/delete-form-hook.md) | `DELETE /api/v1/hooks/form/{hookId}` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Delete Lottery Hook](actions/delete-lottery-hook.md) | `DELETE /api/v1/hooks/lottery/{hookId}` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Delete Quiz Hook](actions/delete-quiz-hook.md) | `DELETE /api/v1/hooks/quiz/{hookId}` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Delete Signal](actions/delete-signal.md) | `DELETE /api/v1/signals/{signalId}` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Delete Signal Hook](actions/delete-signal-hook.md) | `DELETE /api/v1/hooks/{hookId}` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Delete Spinner Hook](actions/delete-spinner-hook.md) | `DELETE /api/v1/hooks/spinner/{hookId}` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Get Signal](actions/get-signal.md) | `GET /api/v1/signals/{signalId}` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Get Site Script Id](actions/get-site-script-id.md) | `GET /api/v1/sites/ScriptId` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [List Easter Egg Hooks](actions/list-easter-egg-hooks.md) | `GET /api/v1/hooks/easterEgg` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [List Feedback Hooks](actions/list-feedback-hooks.md) | `GET /api/v1/hooks/feedback` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [List Form Hooks](actions/list-form-hooks.md) | `GET /api/v1/hooks/form` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [List Lottery Hooks](actions/list-lottery-hooks.md) | `GET /api/v1/hooks/lottery` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [List Lottery Leads](actions/list-lottery-leads.md) | `GET /api/v1/leads/lottery` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [List Quiz Hooks](actions/list-quiz-hooks.md) | `GET /api/v1/hooks/quiz` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [List Signal Hooks](actions/list-signal-hooks.md) | `GET /api/v1/hooks` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [List Signal Leads](actions/list-signal-leads.md) | `GET /api/v1/leads` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [List Signals](actions/list-signals.md) | `GET /api/v1/signals` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [List Spinner Hooks](actions/list-spinner-hooks.md) | `GET /api/v1/hooks/spinner` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Test API Key Authentication](actions/test-api-key-authentication.md) | `GET /api/v1/test` | [docs](https://app.hoversignal.com/docs/ui/index) |
| [Update Signal](actions/update-signal.md) | `PATCH /api/v1/signals/{signalId}` | [docs](https://app.hoversignal.com/docs/ui/index) |
