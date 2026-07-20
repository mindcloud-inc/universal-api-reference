# PeakIDX: Native API Reference

A consolidated summary of PeakIDX's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://docs.peakidx.com/api/
- **API base URL:** `https://account.peakidxsites.com`

## Authentication

### API Key

Use your PeakIDX API key plus tenant site metadata. PeakIDX requires query-parameter auth and tenant-specific site identifiers rather than bearer auth.

### Credentials

- **API Key:** `apiKey` · required · Your PeakIDX API key from the site Admin > API Key screen. This value is sent as the documented PeakIDX query parameter.
- **Site Name:** `siteName` · required · Your PeakIDX site subdomain name used in URLs like https://YOUR-SITE-NAME.peakidxsites.com/.
- **IDX Site ID:** `idxSiteId` · required · Your numeric PeakIDX site identifier required by the lead management endpoints on account.peakidxsites.com.

[Official authentication documentation](https://docs.peakidx.com/api/lead-management-api)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Or Update Lead](actions/create-or-update-lead.md) | `POST https://account.peakidxsites.com/lead-api/create-lead` | [docs](https://docs.peakidx.com/api/lead-management-api#create-lead) |
| [Get Search Criteria](actions/get-search-criteria.md) | `GET https://{{credentials.siteName}}.peakidxsites.com/search-criteria/` | [docs](https://docs.peakidx.com/api/search-criteria-api) |
| [List New Leads](actions/list-new-leads.md) | `GET https://account.peakidxsites.com/lead-api/new-leads` | [docs](https://docs.peakidx.com/api/lead-management-api#new-leads) |
| [List Search Results](actions/list-search-results.md) | `GET https://{{credentials.siteName}}.peakidxsites.com/search-results-api/:searchEmbedId` | [docs](https://docs.peakidx.com/api/search-results-api) |
