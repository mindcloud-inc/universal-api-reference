# Track Conversion with Crazy Egg

## Endpoint

- **Method:** `POST`
- **Path:** `https://track.crazyegg.com/api/v1`
- **Base URL:** `https://app.crazyegg.com/api/v2`
- **Official documentation:** [Track Conversion](https://support.crazyegg.com/knowledge-base/conversion-tracking-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `goalConversions[].goalName` | body | `string` | yes |
| `goalConversions[].userIdentifier` | body | `string` | yes |
| `goalConversions[].url` | body | `string` | no |
| `goalConversions[].value` | body | `number` | no |
| `goalConversions[].currency` | body | `string` | no |
| `goalConversions[].visitCount` | body | `number` | no |
| `goalConversions[].landingPage` | body | `string` | no |
| `goalConversions[].referrer` | body | `string` | no |
| `goalConversions[].country` | body | `string` | no |
| `goalConversions[].userAgent` | body | `string` | no |
| `goalConversions[].timestamp` | body | `string` | no |
| `goalConversions[].utmParams.source` | body | `string` | no |
| `goalConversions[].utmParams.medium` | body | `string` | no |
| `goalConversions[].utmParams.term` | body | `string` | no |
| `goalConversions[].utmParams.content` | body | `string` | no |
| `goalConversions[].utmParams.campaign` | body | `string` | no |
| `goalConversions[].customData` | body | `object` | no |
