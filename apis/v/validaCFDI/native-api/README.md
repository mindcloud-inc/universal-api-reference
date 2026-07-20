# ValidaCFDI: Native API Reference

A consolidated summary of ValidaCFDI's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://valida-cfdi.com.mx/docs/api
- **API base URL:** `https://api.valida-cfdi.com.mx/v1`

## Authentication

### API Key

Authenticate requests with your ValidaCFDI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://valida-cfdi.com.mx/docs/api)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Test API Connection](actions/test-api-connection.md) | `GET /zapier/test` | [docs](https://valida-cfdi.com.mx/docs/api) |
| [Validate CFDI by UUID](actions/validate-cfdi-by-uuid.md) | `POST /validate` | [docs](https://valida-cfdi.com.mx/docs/api) |
| [Validate CFDI from PDF](actions/validate-cfdi-from-pdf.md) | `POST /validate/pdf` | [docs](https://valida-cfdi.com.mx/docs/api) |
