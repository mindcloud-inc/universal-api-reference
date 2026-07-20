# Captain Data: Native API Reference

A consolidated summary of Captain Data's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://docs.captaindata.com/v1/introduction
- **API base URL:** `https://api.captaindata.com/v1`

## Authentication

### API Key

Use your Captain Data workspace API key. Requests send the stored secret as the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required · Captain Data workspace API key from Settings > Developers. The app sends it as X-API-Key on every request.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://support.captaindata.com/en/articles/11587198-how-to-get-an-api-key)

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Enrich Company](actions/enrich-company.md) | `GET /companies/enrich` | [docs](https://docs.captaindata.com/v1/api/companies/enrich) |
| [Enrich People](actions/enrich-people.md) | `GET /people/enrich` | [docs](https://docs.captaindata.com/v1/api/people/enrich) |
| [Find Company](actions/find-company.md) | `GET /companies/find` | [docs](https://docs.captaindata.com/v1/api/companies/find) |
| [Find Company Employees](actions/find-company-employees.md) | `GET /companies/:company_uid/employees` | [docs](https://docs.captaindata.com/v1/api/companies/find-employees) |
| [Find People](actions/find-people.md) | `GET /people/find` | [docs](https://docs.captaindata.com/v1/api/people/find) |
| [Get Quotas](actions/get-quotas.md) | `GET /quotas` | [docs](https://docs.captaindata.com/v1/api/quotas) |
| [Search Companies](actions/search-companies.md) | `GET /companies/search` | [docs](https://docs.captaindata.com/v1/api/companies/search) |
| [Search People](actions/search-people.md) | `GET /people/search` | [docs](https://docs.captaindata.com/v1/api/people/search) |
