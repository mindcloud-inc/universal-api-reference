# SitesManager update Site with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [SitesManager update Site](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `siteName` | body | `string` | no | Matomo API parameter. |
| `urls` | body | `string` | no | Matomo API parameter. |
| `ecommerce` | body | `string` | no | Matomo API parameter. |
| `siteSearch` | body | `string` | no | Matomo API parameter. |
| `searchKeywordParameters` | body | `string` | no | Matomo API parameter. |
| `searchCategoryParameters` | body | `string` | no | Matomo API parameter. |
| `excludedIps` | body | `string` | no | Matomo API parameter. |
| `excludedQueryParameters` | body | `string` | no | Matomo API parameter. |
| `timezone` | body | `string` | no | Matomo API parameter. |
| `currency` | body | `string` | no | Matomo API parameter. |
| `group` | body | `string` | no | Matomo API parameter. |
| `startDate` | body | `string` | no | Matomo API parameter. |
| `excludedUserAgents` | body | `string` | no | Matomo API parameter. |
| `keepURLFragments` | body | `string` | no | Matomo API parameter. |
| `type` | body | `string` | no | Matomo API parameter. |
| `settingValues` | body | `string` | no | Matomo API parameter. |
| `excludeUnknownUrls` | body | `string` | no | Matomo API parameter. |
| `excludedReferrers` | body | `string` | no | Matomo API parameter. |
