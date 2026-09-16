# BarTender: Native API Reference

A consolidated summary of BarTender's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://help.seagullscientific.com/BarTenderCloud/Help/en/Content/API/API_Doc_BTC_API_Documentation_LP.htm
- **OpenAPI specification:** https://am1.bartendercloud.com/api-gateway/swagger/ActionsServiceDocument/swagger.yaml
- **API base URL:** `https://auth.{region}.bartendercloud.com`

## Authentication

### Password-based OAuth

Use BarTender Cloud password-based OAuth access to obtain bearer tokens for REST API calls.

### Credentials

- **Region:** `region` · required · Choose the region where your BarTender Cloud organization is hosted. · Allowed values: `am1`, `ap1`, `eu1`.
- **Organization Domain ID:** `organizationDnsName` · required · Enter the Organization Domain ID used in BarTender Cloud token requests.
- **Application ID:** `clientId` · required · Application ID from the password-based API registration in BarTender Cloud.
- **Application Secret:** `clientSecret` · required · Application secret from the password-based API registration in BarTender Cloud.
- **Username:** `username` · required · BarTender Cloud username with password-based API access allowed.
- **Password:** `password` · required · Password for the BarTender Cloud user with password-based API access allowed.

[Official authentication documentation](https://help.seagullscientific.com/bartendercloud/help/en/content/API/API_Automation_BIDS_PWB_Example.htm)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `MindCloud/1.0` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | `GET /connect/userinfo` | [docs](https://auth.am1.bartendercloud.com/.well-known/openid-configuration) |
