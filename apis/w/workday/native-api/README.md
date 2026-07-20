# Workday: Native API Reference

A consolidated summary of Workday's API configuration, with links to official documentation.

- **Official docs:** https://community.workday.com/sites/default/files/file-hosting/restapi/index.html
- **API base URL:** `{restAPIBaseURL}/`

## Authentication

### Custom

### Credentials

- **Time Tracking REST API Base URL:** `restAPIBaseURL` · required · Use the full Workday timeTracking v5 service base URL for your tenant, for example: https://services1.wd501.myworkday.com/ccx/api/timeTracking/v5/marianienterprises
- **Token Endpoint:** `tokenEndpoint` · optional · This looks something like: 
https://services1.wd501.myworkday.com/ccx/oauth2/mycompany/token
- **Client ID:** `clientID` · optional
- **Client Secret:** `clientSecret` · optional
- **Refresh Token:** `refreshToken` · optional
- **Person REST API Base URL:** `personRestAPIBaseURL` · required · Use the full Workday person v4 service base URL for your tenant, for example: https://services1.wd501.myworkday.com/ccx/api/person/v4/marianienterprises
- **Tenant:** `tenant` · optional · If your REST API endpoint is https://services1.wd501.myworkday.com/ccx/api/v1/mycompany,
then your tenant is "mycompany"

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `offset` in the query string as the record offset; numbering starts at 0.
