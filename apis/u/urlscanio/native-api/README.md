# urlscan.io: Native API Reference

A consolidated summary of urlscan.io's API configuration and 50 documented operations, with links to official documentation.

- **Official docs:** https://docs.urlscan.io/guides/quickstart
- **OpenAPI specification:** https://docs.urlscan.io/apis/urlscan-openapi
- **API base URL:** `https://urlscan.io`

## Authentication

### API Key

Use a urlscan.io API key created in Settings & API. The runtime sends the stored key in the provider-required API-Key header.

### Credentials

- **API Key:** `apiKey` · required · Your urlscan.io API key from Settings & API. The runtime sends this value as the API-Key header.

Send these headers with each API request:

```http
API-Key: <apiKey>
```

[Official authentication documentation](https://docs.urlscan.io/guides/quickstart)

## Endpoints (50 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Close Incident](actions/close-incident.md) | `PUT /api/v1/user/incidents/{incidentId}/close` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/incidents/closeincident.md) |
| [Copy Incident](actions/copy-incident.md) | `POST /api/v1/user/incidents/{incidentId}/copy` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/incidents/copyincident.md) |
| [Create Channel](actions/create-channel.md) | `POST /api/v1/user/channels/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/channels/channelscreate.md) |
| [Create Incident](actions/create-incident.md) | `POST /api/v1/user/incidents` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/incidents/createincident.md) |
| [Create Saved Search](actions/create-saved-search.md) | `POST /api/v1/user/searches/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/saved-searches/savedsearchescreate.md) |
| [Create Subscription](actions/create-subscription.md) | `POST /api/v1/user/subscriptions/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/subscriptions/subscriptionscreate.md) |
| [Delete Saved Search](actions/delete-saved-search.md) | `DELETE /api/v1/user/searches/{searchId}/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/saved-searches/savedsearchesdelete.md) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /api/v1/user/subscriptions/{subscriptionId}/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/subscriptions/subscriptionsdelete.md) |
| [Discard Live Scan](actions/discard-live-scan.md) | `DELETE /api/v1/livescan/{scannerId}/{scanId}/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/live-scanning/livescandiscard.md) |
| [Download File](actions/download-file.md) | `GET /downloads/{fileHash}` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/files/downloadfile.md) |
| [Fork Incident](actions/fork-incident.md) | `POST /api/v1/user/incidents/{incidentId}/fork` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/incidents/forkincident.md) |
| [Get Channel](actions/get-channel.md) | `GET /api/v1/user/channels/{channelId}` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/channels/channelsget.md) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v1/pro/username` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/generic/prousername.md) |
| [Get Data Dump Link](actions/get-data-dump-link.md) | `GET /api/v1/datadump/link/{path}` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/data-dumps/datadumplink.md) |
| [Get DOM Snapshot](actions/get-dom-snapshot.md) | `GET /dom/{scanId}/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/scanning/dom.md) |
| [Get Hostname History](actions/get-hostname-history.md) | `GET /api/v1/hostname/{hostname}` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/hostnames/hostnamehistory.md) |
| [Get Incident](actions/get-incident.md) | `GET /api/v1/user/incidents/{incidentId}` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/incidents/getincident.md) |
| [Get Incident States](actions/get-incident-states.md) | `GET /api/v1/user/incidentstates/{incidentId}/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/incidents/getincidentstates.md) |
| [Get Live Scan Resource](actions/get-live-scan-resource.md) | `GET /api/v1/livescan/{scannerId}/{resourceType}/{resourceId}` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/live-scanning/livescangetresource.md) |
| [Get Malicious Lookup](actions/get-malicious-lookup.md) | `GET /api/v1/malicious/{type}/{value}` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/malicious/maliciouslookup.md) |
| [Get Phishfeed Results](actions/get-phishfeed-results.md) | `GET /api/v1/pro/phishfeed` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/search/phishfeed.md) |
| [Get Quotas](actions/get-quotas.md) | `GET /api/v1/quotas` | [docs](https://docs.urlscan.io/apis/urlscan-openapi) |
| [Get Response Content](actions/get-response-content.md) | `GET /responses/{fileHash}/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/scanning/response.md) |
| [Get Saved Search Results](actions/get-saved-search-results.md) | `GET /api/v1/user/searches/{searchId}/results/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/saved-searches/savedsearchesresult.md) |
| [Get Scan Result](actions/get-scan-result.md) | `GET /api/v1/result/{scanId}/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/scanning/resultapi.md) |
| [Get Screenshot](actions/get-screenshot.md) | `GET /screenshots/{scanId}.png` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/scanning/screenshot.md) |
| [Get Similar Results](actions/get-similar-results.md) | `GET /api/v1/pro/result/{scanId}/similar/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/search/similarsearch.md) |
| [Get Subscription Results](actions/get-subscription-results.md) | `GET /api/v1/user/subscriptions/{subscriptionId}/results/{datasource}/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/subscriptions/subscriptionsresults.md) |
| [List Available Brands](actions/list-available-brands.md) | `GET /api/v1/pro/availableBrands` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/brands/availablebrands.md) |
| [List Available Countries](actions/list-available-countries.md) | `GET /api/v1/availableCountries` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/scanning/availablecountries.md) |
| [List Brand Summary](actions/list-brand-summary.md) | `GET /api/v1/pro/brands` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/brands/brandsummary.md) |
| [List Channels](actions/list-channels.md) | `GET /api/v1/user/channels/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/channels/channels.md) |
| [List Data Dump Files](actions/list-data-dump-files.md) | `GET /api/v1/datadump/list/{timeWindow}/{fileType}/{date}` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/data-dumps/datadumplist.md) |
| [List Live Scanners](actions/list-live-scanners.md) | `GET /api/v1/livescan/scanners/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/live-scanning/livescanscanners.md) |
| [List Saved Searches](actions/list-saved-searches.md) | `GET /api/v1/user/searches/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/saved-searches/savedsearches.md) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /api/v1/user/subscriptions/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/subscriptions/subscriptions.md) |
| [List User Agents](actions/list-user-agents.md) | `GET /api/v1/userAgents` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/scanning/useragents.md) |
| [List Watchable Attributes](actions/list-watchable-attributes.md) | `GET /api/v1/user/watchableAttributes` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/incidents/getwatchableattributes.md) |
| [Reset Result Visibility](actions/reset-result-visibility.md) | `DELETE /api/v1/result/{scanId}/visibility/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/scanning/deleteresultvisibility.md) |
| [Restart Incident](actions/restart-incident.md) | `PUT /api/v1/user/incidents/{incidentId}/restart` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/incidents/restartincident.md) |
| [Run Live Scan](actions/run-live-scan.md) | `POST /api/v1/livescan/{scannerId}/scan/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/live-scanning/livescanscan.md) |
| [Search Historical Results](actions/search-historical-results.md) | `GET /api/v1/search` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/search/search.md) |
| [Store Live Scan](actions/store-live-scan.md) | `PUT /api/v1/livescan/{scannerId}/{scanId}/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/live-scanning/livescanstore.md) |
| [Submit Live Scan Task](actions/submit-live-scan-task.md) | `POST /api/v1/livescan/{scannerId}/task/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/live-scanning/livescantask.md) |
| [Submit Scan](actions/submit-scan.md) | `POST /api/v1/scan` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/scanning/submitscan.md) |
| [Update Channel](actions/update-channel.md) | `PUT /api/v1/user/channels/{channelId}` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/channels/channelsupdate.md) |
| [Update Incident](actions/update-incident.md) | `PUT /api/v1/user/incidents/{incidentId}` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/incidents/updateincident.md) |
| [Update Result Visibility](actions/update-result-visibility.md) | `PUT /api/v1/result/{scanId}/visibility/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/scanning/updateresultvisibility.md) |
| [Update Saved Search](actions/update-saved-search.md) | `PUT /api/v1/user/searches/{searchId}/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/saved-searches/savedsearchesupdate.md) |
| [Update Subscription](actions/update-subscription.md) | `PUT /api/v1/user/subscriptions/{subscriptionId}/` | [docs](https://docs.urlscan.io/apis/urlscan-openapi/subscriptions/subscriptionsget.md) |
