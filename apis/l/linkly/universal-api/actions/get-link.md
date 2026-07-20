# Linkly: Get Link

Retrieves a link from Linkly.

```
GET https://connect.mindcloud.co/v1/universal/linkly/latest/actions/get-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkly/latest/actions/get-link?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkly/latest/actions/get-link?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The id of the Link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockBots": true,
      "bodyTags": "string",
      "cloaking": true,
      "deleted": true,
      "domain": "string",
      "enabled": true,
      "expiryClicks": 1,
      "expiryDatetime": "string",
      "expiryDestination": "string",
      "fbPixelId": "string",
      "forwardParams": true,
      "fullUrl": "https://example.com",
      "ga4TagId": "string",
      "gtmId": "string",
      "headTags": "string",
      "hideReferrer": true,
      "id": 1,
      "insertedAt": "string",
      "linkifyWords": "https://example.com",
      "name": "Ava Chen",
      "note": "string",
      "ogDescription": "string",
      "ogImage": "string",
      "ogTitle": "string",
      "publicAnalytics": true,
      "replacements": "string",
      "rules": [
        {}
      ],
      "skipSocialCrawlerTracking": true,
      "slug": "string",
      "spam": true,
      "url": "https://example.com",
      "utmCampaign": "string",
      "utmContent": "string",
      "utmMedium": "string",
      "utmSource": "string",
      "utmTerm": "string",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockBots` | boolean | Whether bots are blocked. |
| `bodyTags` | string | Custom body tags. |
| `cloaking` | boolean | Whether cloaking is enabled. |
| `deleted` | boolean | Whether the link is deleted. |
| `domain` | string | Domain used by the short link. |
| `enabled` | boolean | Whether the link is enabled. |
| `expiryClicks` | number | Expiry click threshold when configured. |
| `expiryDatetime` | string | Expiry timestamp when configured. |
| `expiryDestination` | string | Destination used after expiry when configured. |
| `fbPixelId` | string | Facebook Pixel ID when configured. |
| `forwardParams` | boolean | Whether query parameters are forwarded. |
| `fullUrl` | string | Shortened Linkly URL. |
| `ga4TagId` | string | GA4 tag ID when configured. |
| `gtmId` | string | Google Tag Manager ID when configured. |
| `headTags` | string | Custom head tags. |
| `hideReferrer` | boolean | Whether referrer hiding is enabled. |
| `id` | number | Link ID. |
| `insertedAt` | string | Creation timestamp. |
| `linkifyWords` | string | Linkify words configuration. |
| `name` | string | Optional link name. |
| `note` | string | Optional internal note. |
| `ogDescription` | string | Open Graph description. |
| `ogImage` | string | Open Graph image URL. |
| `ogTitle` | string | Open Graph title. |
| `publicAnalytics` | boolean | Whether public analytics is enabled. |
| `replacements` | string | Replacement rules summary. |
| `rules` | array<object> | Redirect rule definitions. |
| `skipSocialCrawlerTracking` | boolean | Whether social crawler tracking is skipped. |
| `slug` | string | Optional slug value when available. |
| `spam` | boolean | Whether the link is marked as spam. |
| `url` | string | Destination URL. |
| `utmCampaign` | string | UTM campaign value. |
| `utmContent` | string | UTM content value. |
| `utmMedium` | string | UTM medium value. |
| `utmSource` | string | UTM source value. |
| `utmTerm` | string | UTM term value. |
| `workspaceId` | number | Workspace ID that owns the link. |

## Native endpoint

Through the native Linkly API, this operation is `GET /link/:id` (base URL `https://app.linklyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link.md) for the provider-specific parameters and requirements.

