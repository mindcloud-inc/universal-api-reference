# BunnyCDN: Native API Reference

A consolidated summary of BunnyCDN's API configuration and 87 documented operations, with links to official documentation.

- **Official docs:** https://docs.bunny.net/reference/bunnynet-api-overview
- **OpenAPI specification:** https://docs.bunny.net/openapi
- **API base URL:** `https://api.bunny.net`

## Authentication

### AccessKey Header

Use your bunny.net account API key as the Bunny Core API AccessKey header. This app does not use bearer authorization.

### Credentials

- **API Key:** `apiKey` · required · Your bunny.net account API key used for the Bunny Core API AccessKey header.

Send these headers with each API request:

```http
AccessKey: <apiKey>
```

[Official authentication documentation](https://docs.bunny.net/reference/bunnynet-api-overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (87 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Custom Certificate](actions/add-custom-certificate.md) | `POST /pullzone/:id/addCertificate` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Custom Hostname](actions/add-custom-hostname.md) | `POST /pullzone/:id/addHostname` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add DNS Record](actions/add-dns-record.md) | `PUT /dnszone/:zoneId/records` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add DNS Zone](actions/add-dns-zone.md) | `POST /dnszone` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Live Thumbnail](actions/add-live-thumbnail.md) | `PUT /videolibrary/:id/live/thumbnail` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Live Watermark](actions/add-live-watermark.md) | `PUT /videolibrary/:id/live/watermark` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Or Update Edge Rule](actions/add-or-update-edge-rule.md) | `POST /pullzone/:pullZoneId/edgerules/addOrUpdate` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Pull Zone](actions/add-pull-zone.md) | `POST /pullzone` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Pull Zone Allowed Referer](actions/add-pull-zone-allowed-referer.md) | `POST /pullzone/:id/addAllowedReferrer` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Pull Zone Blocked IP](actions/add-pull-zone-blocked-ip.md) | `POST /pullzone/:id/addBlockedIp` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Pull Zone Blocked Referer](actions/add-pull-zone-blocked-referer.md) | `POST /pullzone/:id/addBlockedReferrer` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Storage Zone](actions/add-storage-zone.md) | `POST /storagezone` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Video Library](actions/add-video-library.md) | `POST /videolibrary` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Video Library Allowed Referer](actions/add-video-library-allowed-referer.md) | `POST /videolibrary/:id/addAllowedReferrer` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Video Library Blocked Referer](actions/add-video-library-blocked-referer.md) | `POST /videolibrary/:id/addBlockedReferrer` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Add Video Library Watermark](actions/add-video-library-watermark.md) | `PUT /videolibrary/:id/watermark` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Change Hostname Private Key Type](actions/change-hostname-private-key-type.md) | `POST /pullzone/:id/updatePrivateKeyType` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Check DNS Zone Availability](actions/check-dns-zone-availability.md) | `POST /dnszone/checkavailability` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Check Pull Zone Availability](actions/check-pull-zone-availability.md) | `POST /pullzone/checkavailability` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Check Storage Zone Availability](actions/check-storage-zone-availability.md) | `POST /storagezone/checkavailability` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Close Account](actions/close-account.md) | `POST /user/closeaccount` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Delete DNS Record](actions/delete-dns-record.md) | `DELETE /dnszone/:zoneId/records/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Delete DNS Zone](actions/delete-dns-zone.md) | `DELETE /dnszone/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Delete Edge Rule](actions/delete-edge-rule.md) | `DELETE /pullzone/:pullZoneId/edgerules/:edgeRuleId` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Delete Live Thumbnail](actions/delete-live-thumbnail.md) | `DELETE /videolibrary/:id/live/thumbnail` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Delete Live Watermark](actions/delete-live-watermark.md) | `DELETE /videolibrary/:id/live/watermark` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Delete Pull Zone](actions/delete-pull-zone.md) | `DELETE /pullzone/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Delete Storage Zone](actions/delete-storage-zone.md) | `DELETE /storagezone/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Delete Video Library](actions/delete-video-library.md) | `DELETE /videolibrary/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Delete Video Library Watermark](actions/delete-video-library-watermark.md) | `DELETE /videolibrary/:id/watermark` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Disable DNSSEC](actions/disable-dnssec.md) | `DELETE /dnszone/:id/dnssec` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Download Payment Request Invoice PDF](actions/download-payment-request-invoice-pdf.md) | `GET /billing/payment-request-invoice/:id/pdf` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Enable DNSSEC](actions/enable-dnssec.md) | `POST /dnszone/:id/dnssec` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Export DNS Zone](actions/export-dns-zone.md) | `GET /dnszone/:id/export` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Affiliate Details](actions/get-affiliate-details.md) | `GET /billing/affiliate` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Billing Details](actions/get-billing-details.md) | `GET /billing` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Billing Summary](actions/get-billing-summary.md) | `GET /billing/summary` | [docs](https://docs.bunny.net/reference/billingpublic_getsummary) |
| [Get Billing Summary Document](actions/get-billing-summary-document.md) | `GET /billing/summary/:billingRecordId/pdf` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Country List](actions/get-country-list.md) | `GET /country` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get DNS Query Statistics](actions/get-dns-query-statistics.md) | `GET /dnszone/:id/statistics` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get DNS Record Scan Result](actions/get-dns-record-scan-result.md) | `GET /dnszone/:zoneId/records/scan` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get DNS Zone](actions/get-dns-zone.md) | `GET /dnszone/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Optimizer Statistics](actions/get-optimizer-statistics.md) | `GET /pullzone/:pullZoneId/optimizer/statistics` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Origin Shield Queue Statistics](actions/get-origin-shield-queue-statistics.md) | `GET /pullzone/:pullZoneId/originshield/queuestatistics` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Pending Payment Requests](actions/get-pending-payment-requests.md) | `GET /billing/payment-requests` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Pull Zone](actions/get-pull-zone.md) | `GET /pullzone/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Region List](actions/get-region-list.md) | `GET /region` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get SafeHop Statistics](actions/get-safe-hop-statistics.md) | `GET /pullzone/:pullZoneId/safehop/statistics` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Statistics](actions/get-statistics.md) | `GET /statistics` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Storage Zone](actions/get-storage-zone.md) | `GET /storagezone/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Storage Zone Statistics](actions/get-storage-zone-statistics.md) | `GET /storagezone/:id/statistics` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get User Audit Log](actions/get-user-audit-log.md) | `GET /user/audit/:date` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Video Library](actions/get-video-library.md) | `GET /videolibrary/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Video Library DRM Statistics](actions/get-video-library-drm-statistics.md) | `GET /videolibrary/:id/drm/statistics` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Video Library Languages](actions/get-video-library-languages.md) | `GET /videolibrary/languages` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Get Video Library Transcribing Statistics](actions/get-video-library-transcribing-statistics.md) | `GET /videolibrary/:id/transcribing/statistics` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Global Search](actions/global-search.md) | `GET /search` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Import DNS Records](actions/import-dns-records.md) | `POST /dnszone/:zoneId/import` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Issue Wildcard Certificate](actions/issue-wildcard-certificate.md) | `POST /dnszone/:zoneId/certificate/issue` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [List API Keys](actions/list-api-keys.md) | `GET /apikey` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [List DNS Zones](actions/list-dns-zones.md) | `GET /dnszone` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [List Pull Zones](actions/list-pull-zones.md) | `GET /pullzone` | [docs](https://docs.bunny.net/reference/pullzonepublic_index) |
| [List Storage Zones](actions/list-storage-zones.md) | `GET /storagezone` | [docs](https://docs.bunny.net/reference/storagezonepublic_index) |
| [List Video Libraries](actions/list-video-libraries.md) | `GET /videolibrary` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Load Free Certificate](actions/load-free-certificate.md) | `GET /pullzone/loadFreeCertificate` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Purge Cache](actions/purge-cache.md) | `POST /pullzone/:id/purgeCache` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Purge URL](actions/purge-url.md) | `POST /purge` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Remove Certificate](actions/remove-certificate.md) | `DELETE /pullzone/:id/removeCertificate` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Remove Custom Hostname](actions/remove-custom-hostname.md) | `DELETE /pullzone/:id/removeHostname` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Remove Pull Zone Allowed Referer](actions/remove-pull-zone-allowed-referer.md) | `POST /pullzone/:id/removeAllowedReferrer` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Remove Pull Zone Blocked IP](actions/remove-pull-zone-blocked-ip.md) | `POST /pullzone/:id/removeBlockedIp` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Remove Pull Zone Blocked Referer](actions/remove-pull-zone-blocked-referer.md) | `POST /pullzone/:id/removeBlockedReferrer` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Remove Video Library Allowed Referer](actions/remove-video-library-allowed-referer.md) | `POST /videolibrary/:id/removeAllowedReferrer` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Remove Video Library Blocked Referer](actions/remove-video-library-blocked-referer.md) | `POST /videolibrary/:id/removeBlockedReferrer` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Reset Storage Zone Password](actions/reset-storage-zone-password.md) | `POST /storagezone/:id/resetPassword` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Reset Storage Zone Read Only Password](actions/reset-storage-zone-read-only-password.md) | `POST /storagezone/resetReadOnlyPassword` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Reset Token Key](actions/reset-token-key.md) | `POST /pullzone/:id/resetSecurityKey` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Reset Video Library API Key](actions/reset-video-library-api-key.md) | `POST /videolibrary/:id/resetApiKey` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Reset Video Library Read Only API Key](actions/reset-video-library-read-only-api-key.md) | `POST /videolibrary/:id/resetReadOnlyApiKey` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Set Edge Rule Enabled](actions/set-edge-rule-enabled.md) | `POST /pullzone/:pullZoneId/edgerules/:edgeRuleId/setEdgeRuleEnabled` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Set Force SSL](actions/set-force-ssl.md) | `POST /pullzone/:id/setForceSSL` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Trigger DNS Record Scan](actions/trigger-dns-record-scan.md) | `POST /dnszone/records/scan` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Update DNS Record](actions/update-dns-record.md) | `POST /dnszone/:zoneId/records/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Update DNS Zone](actions/update-dns-zone.md) | `POST /dnszone/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Update Pull Zone](actions/update-pull-zone.md) | `POST /pullzone/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Update Storage Zone](actions/update-storage-zone.md) | `POST /storagezone/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
| [Update Video Library](actions/update-video-library.md) | `POST /videolibrary/:id` | [docs](https://docs.bunny.net/reference/bunnynet-api-overview) |
