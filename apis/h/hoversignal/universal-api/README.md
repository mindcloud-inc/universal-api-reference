# <img src="https://images.mindcloud.co/apps/icons/hoversignal_1776262087128.png" alt="Hoversignal logo" width="28" height="28"> Hoversignal: Universal API

Hoversignal API integration for hooks, signals, and lead access.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hoversignal/latest
- **Category:** Marketing / Advertising
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hoversignal.com
- **Vendor API docs:** https://app.hoversignal.com/docs/ui/index

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test API Key Authentication](actions/test-api-key-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/test-api-key-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Script Id](actions/get-site-script-id.md) | GET |  |

### Easter Egg Hook

| Action | Method | Description |
| --- | --- | --- |
| [Create Easter Egg Hook](actions/create-easter-egg-hook.md) | POST |  |
| [Delete Easter Egg Hook](actions/delete-easter-egg-hook.md) | DELETE |  |
| [List Easter Egg Hooks](actions/list-easter-egg-hooks.md) | GET |  |

### Feedback Hook

| Action | Method | Description |
| --- | --- | --- |
| [Create Feedback Hook](actions/create-feedback-hook.md) | POST |  |
| [Delete Feedback Hook](actions/delete-feedback-hook.md) | DELETE |  |
| [List Feedback Hooks](actions/list-feedback-hooks.md) | GET |  |

### Form Hook

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Hook](actions/create-form-hook.md) | POST |  |
| [Delete Form Hook](actions/delete-form-hook.md) | DELETE |  |
| [List Form Hooks](actions/list-form-hooks.md) | GET |  |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [List Signal Leads](actions/list-signal-leads.md) | GET |  |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [List Lottery Leads](actions/list-lottery-leads.md) | GET |  |

### Lottery Hook

| Action | Method | Description |
| --- | --- | --- |
| [Create Lottery Hook](actions/create-lottery-hook.md) | POST |  |
| [Delete Lottery Hook](actions/delete-lottery-hook.md) | DELETE |  |
| [List Lottery Hooks](actions/list-lottery-hooks.md) | GET |  |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Test API Key Authentication](actions/test-api-key-authentication.md) | GET |  |

### Quiz Hook

| Action | Method | Description |
| --- | --- | --- |
| [Create Quiz Hook](actions/create-quiz-hook.md) | POST |  |
| [Delete Quiz Hook](actions/delete-quiz-hook.md) | DELETE |  |
| [List Quiz Hooks](actions/list-quiz-hooks.md) | GET |  |

### Signal

| Action | Method | Description |
| --- | --- | --- |
| [Create Signal](actions/create-signal.md) | POST |  |
| [Delete Signal](actions/delete-signal.md) | DELETE |  |
| [Get Signal](actions/get-signal.md) | GET |  |
| [List Signals](actions/list-signals.md) | GET |  |
| [Update Signal](actions/update-signal.md) | PUT |  |

### Signal Hook

| Action | Method | Description |
| --- | --- | --- |
| [Create Signal Hook](actions/create-signal-hook.md) | POST |  |
| [Delete Signal Hook](actions/delete-signal-hook.md) | DELETE |  |
| [List Signal Hooks](actions/list-signal-hooks.md) | GET |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Spinner Hook](actions/create-spinner-hook.md) | POST |  |
| [Delete Spinner Hook](actions/delete-spinner-hook.md) | DELETE |  |
| [List Spinner Hooks](actions/list-spinner-hooks.md) | GET |  |

