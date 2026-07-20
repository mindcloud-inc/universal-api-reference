# <img src="https://images.mindcloud.co/apps/icons/bunny_1777387518616.png" alt="BunnyCDN logo" width="28" height="28"> BunnyCDN: Universal API

Manage bunny.net account resources including pull zones, storage zones, DNS zones, stream video libraries, billing, search, statistics, and cache purge operations through the Bunny core API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bunnyCDN/latest
- **Category:** IT Operations / DevOps
- **Actions:** 87
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bunny.net
- **Vendor API docs:** https://docs.bunny.net/reference/bunnynet-api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Pull Zones](actions/list-pull-zones.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/list-pull-zones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (87)

### Affiliate

| Action | Method | Description |
| --- | --- | --- |
| [Get Affiliate Details](actions/get-affiliate-details.md) | GET | Retrieves affiliate program details from BunnyCDN. |

### Api Keys

| Action | Method | Description |
| --- | --- | --- |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves account API keys from BunnyCDN. |

### Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [Get User Audit Log](actions/get-user-audit-log.md) | GET | Retrieves BunnyCDN user audit log entries. |

### Billing

| Action | Method | Description |
| --- | --- | --- |
| [Download Payment Request Invoice PDF](actions/download-payment-request-invoice-pdf.md) | GET | Retrieves a BunnyCDN payment request invoice PDF. |
| [Get Billing Details](actions/get-billing-details.md) | GET | Retrieves detailed billing information from BunnyCDN. |
| [Get Billing Summary Document](actions/get-billing-summary-document.md) | GET | Retrieves a BunnyCDN billing summary PDF. |
| [Get Pending Payment Requests](actions/get-pending-payment-requests.md) | GET | Retrieves pending payment requests from BunnyCDN. |

### Billing Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing Summary](actions/get-billing-summary.md) | GET | Retrieves billing summary data from BunnyCDN. |

### Countries

| Action | Method | Description |
| --- | --- | --- |
| [Get Country List](actions/get-country-list.md) | GET | Retrieves the country list from BunnyCDN. |

### Dns Zone

| Action | Method | Description |
| --- | --- | --- |
| [Add DNS Record](actions/add-dns-record.md) | POST | Creates a new DNS record in BunnyCDN. |
| [Add DNS Zone](actions/add-dns-zone.md) | POST | Creates a new DNS zone in BunnyCDN. |
| [Check DNS Zone Availability](actions/check-dns-zone-availability.md) | POST | Checks DNS zone availability in BunnyCDN. |
| [Delete DNS Record](actions/delete-dns-record.md) | DELETE | Deletes an existing DNS record from BunnyCDN. |
| [Delete DNS Zone](actions/delete-dns-zone.md) | DELETE | Deletes an existing DNS zone from BunnyCDN. |
| [Disable DNSSEC](actions/disable-dnssec.md) | DELETE | Disables DNSSEC for a BunnyCDN DNS zone. |
| [Enable DNSSEC](actions/enable-dnssec.md) | PUT | Enables DNSSEC for a BunnyCDN DNS zone. |
| [Export DNS Zone](actions/export-dns-zone.md) | GET | Retrieves a DNS zone export from BunnyCDN. |
| [Get DNS Query Statistics](actions/get-dns-query-statistics.md) | GET | Retrieves DNS query statistics from BunnyCDN. |
| [Get DNS Record Scan Result](actions/get-dns-record-scan-result.md) | GET | Retrieves DNS record scan results from BunnyCDN. |
| [Get DNS Zone](actions/get-dns-zone.md) | GET | Retrieves a DNS zone from BunnyCDN by ID. |
| [Import DNS Records](actions/import-dns-records.md) | POST | Imports DNS records into BunnyCDN DNS zones. |
| [Issue Wildcard Certificate](actions/issue-wildcard-certificate.md) | POST | Issues a wildcard certificate for a BunnyCDN DNS zone. |
| [List DNS Zones](actions/list-dns-zones.md) | GET | Retrieves all DNS zones from BunnyCDN. |
| [Trigger DNS Record Scan](actions/trigger-dns-record-scan.md) | POST | Triggers a DNS record scan in BunnyCDN. |
| [Update DNS Record](actions/update-dns-record.md) | PUT | Updates an existing DNS record in BunnyCDN. |
| [Update DNS Zone](actions/update-dns-zone.md) | PUT | Updates an existing DNS zone in BunnyCDN. |

### Pull Zone

| Action | Method | Description |
| --- | --- | --- |
| [Add Custom Certificate](actions/add-custom-certificate.md) | POST | Adds a custom certificate to a BunnyCDN pull zone. |
| [Add Custom Hostname](actions/add-custom-hostname.md) | POST | Adds a custom hostname to a BunnyCDN pull zone. |
| [Add Or Update Edge Rule](actions/add-or-update-edge-rule.md) | PUT | Adds or updates an edge rule in BunnyCDN. |
| [Add Pull Zone](actions/add-pull-zone.md) | POST | Creates a new pull zone in BunnyCDN. |
| [Add Pull Zone Allowed Referer](actions/add-pull-zone-allowed-referer.md) | POST | Adds an allowed referer to a BunnyCDN pull zone. |
| [Add Pull Zone Blocked IP](actions/add-pull-zone-blocked-ip.md) | POST | Adds a blocked IP to a BunnyCDN pull zone. |
| [Add Pull Zone Blocked Referer](actions/add-pull-zone-blocked-referer.md) | POST | Adds a blocked referer to a BunnyCDN pull zone. |
| [Change Hostname Private Key Type](actions/change-hostname-private-key-type.md) | PUT | Updates a BunnyCDN hostname private key type. |
| [Check Pull Zone Availability](actions/check-pull-zone-availability.md) | POST | Checks pull zone availability in BunnyCDN. |
| [Delete Edge Rule](actions/delete-edge-rule.md) | DELETE | Deletes an edge rule from a BunnyCDN pull zone. |
| [Delete Pull Zone](actions/delete-pull-zone.md) | DELETE | Deletes an existing pull zone from BunnyCDN. |
| [Get Optimizer Statistics](actions/get-optimizer-statistics.md) | GET | Retrieves optimizer usage statistics from BunnyCDN. |
| [Get Origin Shield Queue Statistics](actions/get-origin-shield-queue-statistics.md) | GET | Retrieves origin shield queue statistics from BunnyCDN. |
| [Get Pull Zone](actions/get-pull-zone.md) | GET | Retrieves a pull zone from BunnyCDN by ID. |
| [Get SafeHop Statistics](actions/get-safe-hop-statistics.md) | GET | Retrieves SafeHop traffic statistics from BunnyCDN. |
| [List Pull Zones](actions/list-pull-zones.md) | GET | Retrieves all pull zones from BunnyCDN. |
| [Load Free Certificate](actions/load-free-certificate.md) | GET | Loads a free certificate in BunnyCDN. |
| [Purge Cache](actions/purge-cache.md) | POST | Purges cached content from a BunnyCDN pull zone. |
| [Remove Certificate](actions/remove-certificate.md) | DELETE | Removes a certificate from a BunnyCDN pull zone. |
| [Remove Custom Hostname](actions/remove-custom-hostname.md) | DELETE | Removes a custom hostname from a BunnyCDN pull zone. |
| [Remove Pull Zone Allowed Referer](actions/remove-pull-zone-allowed-referer.md) | PUT | Removes an allowed referer from a BunnyCDN pull zone. |
| [Remove Pull Zone Blocked IP](actions/remove-pull-zone-blocked-ip.md) | PUT | Removes a blocked IP from a BunnyCDN pull zone. |
| [Remove Pull Zone Blocked Referer](actions/remove-pull-zone-blocked-referer.md) | PUT | Removes a blocked referer from a BunnyCDN pull zone. |
| [Reset Token Key](actions/reset-token-key.md) | PUT | Resets a BunnyCDN pull zone token key. |
| [Set Edge Rule Enabled](actions/set-edge-rule-enabled.md) | PUT | Updates an edge rule's enabled status in BunnyCDN. |
| [Set Force SSL](actions/set-force-ssl.md) | PUT | Updates force SSL settings for a BunnyCDN pull zone. |
| [Update Pull Zone](actions/update-pull-zone.md) | PUT | Updates an existing pull zone in BunnyCDN. |

### Purge

| Action | Method | Description |
| --- | --- | --- |
| [Purge URL](actions/purge-url.md) | POST | Purges a URL from the BunnyCDN cache. |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [Get Region List](actions/get-region-list.md) | GET | Retrieves the region list from BunnyCDN. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Global Search](actions/global-search.md) | GET | Searches BunnyCDN resources by search term. |

### Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Statistics](actions/get-statistics.md) | GET | Retrieves account usage statistics from BunnyCDN. |

### Storage Zone

| Action | Method | Description |
| --- | --- | --- |
| [Add Storage Zone](actions/add-storage-zone.md) | POST | Creates a new storage zone in BunnyCDN. |
| [Check Storage Zone Availability](actions/check-storage-zone-availability.md) | POST | Checks storage zone availability in BunnyCDN. |
| [Delete Storage Zone](actions/delete-storage-zone.md) | DELETE | Deletes an existing storage zone from BunnyCDN. |
| [Get Storage Zone](actions/get-storage-zone.md) | GET | Retrieves a storage zone from BunnyCDN by ID. |
| [Get Storage Zone Statistics](actions/get-storage-zone-statistics.md) | GET | Retrieves storage zone statistics from BunnyCDN. |
| [List Storage Zones](actions/list-storage-zones.md) | GET | Retrieves all storage zones from BunnyCDN. |
| [Reset Storage Zone Password](actions/reset-storage-zone-password.md) | PUT | Resets a BunnyCDN storage zone password. |
| [Reset Storage Zone Read Only Password](actions/reset-storage-zone-read-only-password.md) | PUT | Resets a BunnyCDN storage zone read-only password. |
| [Update Storage Zone](actions/update-storage-zone.md) | PUT | Updates an existing storage zone in BunnyCDN. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Close Account](actions/close-account.md) | POST | Closes the current BunnyCDN user account. |

### Video Library

| Action | Method | Description |
| --- | --- | --- |
| [Add Live Thumbnail](actions/add-live-thumbnail.md) | POST | Adds a live thumbnail to a BunnyCDN video library. |
| [Add Live Watermark](actions/add-live-watermark.md) | POST | Adds a live watermark to a BunnyCDN video library. |
| [Add Video Library](actions/add-video-library.md) | POST | Creates a new video library in BunnyCDN. |
| [Add Video Library Allowed Referer](actions/add-video-library-allowed-referer.md) | POST | Adds an allowed referer to a BunnyCDN video library. |
| [Add Video Library Blocked Referer](actions/add-video-library-blocked-referer.md) | POST | Adds a blocked referer to a BunnyCDN video library. |
| [Add Video Library Watermark](actions/add-video-library-watermark.md) | POST | Adds a watermark to a BunnyCDN video library. |
| [Delete Live Thumbnail](actions/delete-live-thumbnail.md) | DELETE | Deletes a live thumbnail from a BunnyCDN video library. |
| [Delete Live Watermark](actions/delete-live-watermark.md) | DELETE | Deletes a live watermark from a BunnyCDN video library. |
| [Delete Video Library](actions/delete-video-library.md) | DELETE | Deletes an existing video library from BunnyCDN. |
| [Delete Video Library Watermark](actions/delete-video-library-watermark.md) | DELETE | Deletes a watermark from a BunnyCDN video library. |
| [Get Video Library](actions/get-video-library.md) | GET | Retrieves a video library from BunnyCDN by ID. |
| [Get Video Library DRM Statistics](actions/get-video-library-drm-statistics.md) | GET | Retrieves video library DRM statistics from BunnyCDN. |
| [Get Video Library Languages](actions/get-video-library-languages.md) | GET | Retrieves video library languages from BunnyCDN. |
| [Get Video Library Transcribing Statistics](actions/get-video-library-transcribing-statistics.md) | GET | Retrieves video library transcribing statistics from BunnyCDN. |
| [List Video Libraries](actions/list-video-libraries.md) | GET | Retrieves all video libraries from BunnyCDN. |
| [Remove Video Library Allowed Referer](actions/remove-video-library-allowed-referer.md) | PUT | Removes an allowed referer from a BunnyCDN video library. |
| [Remove Video Library Blocked Referer](actions/remove-video-library-blocked-referer.md) | PUT | Removes a blocked referer from a BunnyCDN video library. |
| [Reset Video Library API Key](actions/reset-video-library-api-key.md) | PUT | Resets a BunnyCDN video library API key. |
| [Reset Video Library Read Only API Key](actions/reset-video-library-read-only-api-key.md) | PUT | Resets a BunnyCDN video library read-only API key. |
| [Update Video Library](actions/update-video-library.md) | PUT | Updates an existing video library in BunnyCDN. |

