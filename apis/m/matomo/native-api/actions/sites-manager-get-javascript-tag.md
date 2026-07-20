# SitesManager get Javascript Tag with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [SitesManager get Javascript Tag](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `piwikUrl` | body | `string` | no | Matomo API parameter. |
| `mergeSubdomains` | body | `string` | no | Matomo API parameter. |
| `groupPageTitlesByDomain` | body | `string` | no | Matomo API parameter. |
| `mergeAliasUrls` | body | `string` | no | Matomo API parameter. |
| `visitorCustomVariables` | body | `string` | no | Matomo API parameter. |
| `pageCustomVariables` | body | `string` | no | Matomo API parameter. |
| `customCampaignNameQueryParam` | body | `string` | no | Matomo API parameter. |
| `customCampaignKeywordParam` | body | `string` | no | Matomo API parameter. |
| `doNotTrack` | body | `string` | no | Matomo API parameter. |
| `disableCookies` | body | `string` | no | Matomo API parameter. |
| `trackNoScript` | body | `string` | no | Matomo API parameter. |
| `crossDomain` | body | `string` | no | Matomo API parameter. |
| `forceMatomoEndpoint` | body | `boolean` | no | Matomo API parameter. |
| `excludedQueryParams` | body | `string` | no | Matomo API parameter. |
| `excludedReferrers` | body | `string` | no | Matomo API parameter. |
| `disableCampaignParameters` | body | `string` | no | Matomo API parameter. |
