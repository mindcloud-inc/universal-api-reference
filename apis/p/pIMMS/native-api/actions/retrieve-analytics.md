# Retrieve Analytics with PIMMS

Retrieves filtered analytics metrics from PIMMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics`
- **Base URL:** `https://api.pimms.io`
- **Official documentation:** [Retrieve Analytics](https://pimms.apidocumentation.com/reference#tag/analytics/GET/analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | query | `string` | no | The type of event to retrieve analytics for. Defaults to `clicks`. |
| `groupBy` | query | `string` | no | The parameter to group the analytics data points by. Defaults to `count` if undefined. |
| `domain` | query | `string` | no | The domain to filter analytics for. |
| `key` | query | `string` | no | The short link slug. |
| `linkId` | query | `string` | no | The unique ID of the short link on PiMMs. |
| `externalId` | query | `string` | no | This is the ID of the link in the your database. Must be prefixed with 'ext_' when passed as a query parameter. |
| `tenantId` | query | `string` | no | The ID of the tenant that created the link inside your system. |
| `programId` | query | `string` | no | The ID of the program to retrieve analytics for. |
| `partnerId` | query | `string` | no | The ID of the partner to retrieve analytics for. |
| `interval` | query | `string` | no | The interval to retrieve analytics for. If undefined, defaults to 24h. |
| `start` | query | `string` | no | The start date and time when to retrieve analytics from. Takes precedence over `interval`. |
| `end` | query | `string` | no | The end date and time when to retrieve analytics from. If not provided, defaults to the current date. Takes precedence over `interval`. |
| `timezone` | query | `string` | no | The IANA time zone code for aligning timeseries granularity (e.g. America/New_York). Defaults to UTC. |
| `country` | query | `string` | no | The country to retrieve analytics for. |
| `city` | query | `string` | no | The city to retrieve analytics for. |
| `region` | query | `string` | no | The ISO 3166-2 region code to retrieve analytics for. |
| `continent` | query | `string` | no | The continent to retrieve analytics for. |
| `device` | query | `string` | no | The device to retrieve analytics for. |
| `browser` | query | `string` | no | The browser to retrieve analytics for. |
| `os` | query | `string` | no | The OS to retrieve analytics for. |
| `trigger` | query | `string` | no | The trigger to retrieve analytics for. If undefined, return both QR and link clicks. |
| `referer` | query | `string` | no | The referer to retrieve analytics for. |
| `refererUrl` | query | `string` | no | The full referer URL to retrieve analytics for. |
| `url` | query | `string` | no | The URL to retrieve analytics for. |
| `tagId` | query | `string` | no | Deprecated. Use `tagIds` instead. The tag ID to retrieve analytics for. |
| `tagIds` | query | `string` | no | The tag IDs to retrieve analytics for. |
| `folderId` | query | `string` | no | The folder ID to retrieve analytics for. If not provided, return analytics for unsorted links. |
| `qr` | query | `boolean` | no | Deprecated. Use the `trigger` field instead. Filter for QR code scans. If true, filter for QR codes only. If false, filter for links only. If undefined, return both. |
| `root` | query | `boolean` | no | Filter for root domains. If true, filter for domains only. If false, filter for links only. If undefined, return both. |
| `utm_source` | query | `string` | no | The UTM source of the short link. |
| `utm_medium` | query | `string` | no | The UTM medium of the short link. |
| `utm_campaign` | query | `string` | no | The UTM campaign of the short link. |
| `utm_term` | query | `string` | no | The UTM term of the short link. |
| `utm_content` | query | `string` | no | The UTM content of the short link. |
