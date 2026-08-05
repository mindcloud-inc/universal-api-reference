# Google Analytics: Native API Reference

A consolidated summary of Google Analytics's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/analytics
- **API base URL:** `https://analyticsdata.googleapis.com/v1beta`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile https://www.googleapis.com/auth/analytics.readonly`.

Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/web-server)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Conversions Report](actions/get-conversions-report.md) | `POST https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd` | [docs](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runReport) |
| [Get Device and Geography Report](actions/get-device-geography-report.md) | `POST https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd` | [docs](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runReport) |
| [Get Ecommerce Report](actions/get-ecommerce-report.md) | `POST https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd` | [docs](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runReport) |
| [Get Engagement Report](actions/get-engagement-report.md) | `POST https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd` | [docs](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runReport) |
| [Get Events and Key Events Report](actions/get-events-key-events-report.md) | `POST https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd` | [docs](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runReport) |
| [Get Landing Pages Report](actions/get-landing-pages-report.md) | `POST https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd` | [docs](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runReport) |
| [Get Pages Report](actions/get-pages-report.md) | `POST https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd` | [docs](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runReport) |
| [Get Property Metadata](actions/get-property-metadata.md) | `GET https://analyticsdata.googleapis.com/v1beta/properties/:propertyId/metadata` | [docs](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/getMetadata) |
| [Get Traffic Acquisition Report](actions/get-traffic-acquisition-report.md) | `POST https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd` | [docs](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runReport) |
| [List Account Summaries](actions/list-account-summaries.md) | `GET https://analyticsadmin.googleapis.com/v1beta/accountSummaries` | [docs](https://developers.google.com/analytics/devguides/config/admin/v1/rest/v1beta/accountSummaries/list) |
| [List Accounts](actions/list-accounts.md) | `GET https://analyticsadmin.googleapis.com/v1beta/accounts` | [docs](https://developers.google.com/analytics/devguides/config/admin/v1/rest/v1beta/accounts/list) |
| [List Properties](actions/list-properties.md) | `GET https://analyticsadmin.googleapis.com/v1beta/properties` | [docs](https://developers.google.com/analytics/devguides/config/admin/v1/rest/v1beta/properties/list) |
| [Run Custom Report](actions/run-custom-report.md) | `POST https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd` | [docs](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runReport) |
| [Run Funnel Report](actions/run-funnel-report.md) | `POST https://analyticsdata.googleapis.com/v1alpha/properties/:propertyId:urlEnd` | [docs](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1alpha/properties/runFunnelReport) |
| [Run Realtime Report](actions/run-realtime-report.md) | `POST https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd` | [docs](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runRealtimeReport) |
