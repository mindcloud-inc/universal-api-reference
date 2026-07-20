# Automate Sales CRM: Native API Reference

A consolidated summary of Automate Sales CRM's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://support.automatebusiness.com/en/category/automate-sales-crm-6px6fi
- **API base URL:** `https://api.automatebusiness.com/functions/v1/`

## Authentication

### API key

Use the API key from Settings > Integration > API in Automate Sales CRM.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.automatebusiness.com/en/article/how-to-integrate-lead-forms-with-automated-crm-app-through-pabbly-ckva8e/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create New Lead V2](actions/create-new-lead-v2.md) | `POST ab-crm-webhook` | [docs](https://support.automatebusiness.com/en/article/how-to-integrate-lead-forms-with-automated-crm-app-through-pabbly-ckva8e/) |
