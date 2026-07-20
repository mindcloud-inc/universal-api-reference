# Linkly: Update Link

Updates an existing link in Linkly.

```
PUT https://connect.mindcloud.co/v1/universal/linkly/latest/actions/update-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/linkly/latest/actions/update-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkly/latest/actions/update-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Link ID. Required to update an existing link. |
| `url` | string | no | Optional destination URL. |
| `name` | string | no | Optional display name for the link. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | no | Optional custom short-code slug. Linkly's current runtime rejects custom slug values in this workspace with `slug must be empty`. |
| `note` | string | no | Optional internal note for the link. |
| `domain` | string | no | Optional domain for the link. |
| `enabled` | boolean | no | Whether the link is enabled. |
| `forward_params` | boolean | no | Whether to forward query parameters to the destination URL. |
| `hide_referrer` | boolean | no | Whether to hide the referrer. |
| `cloaking` | boolean | no | Whether to enable cloaking. |
| `block_bots` | boolean | no | Whether to block bots. |
| `utm_source` | string | no | Optional UTM source parameter. |
| `utm_medium` | string | no | Optional UTM medium parameter. |
| `utm_campaign` | string | no | Optional UTM campaign parameter. |
| `utm_term` | string | no | Optional UTM term parameter. |
| `utm_content` | string | no | Optional UTM content parameter. |
| `rules[]` | array<object> | no | Optional array of redirect rule objects. Use the nested Rules fields below to define each rule. |
| `rules[].what` | string | no | What the redirect rule matches against. |
| `rules[].url` | string | no | Destination URL to use when the rule matches. |
| `rules[].rule_url` | string | no | Source URL or pattern evaluated by the rule when applicable. |
| `rules[].percentage` | string | no | Traffic percentage for percentage-based rules. |
| `rules[].matches` | string | no | Match expression for the redirect rule. |

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

Through the native Linkly API, this operation is `POST /link` (base URL `https://app.linklyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-link.md) for the provider-specific parameters and requirements.

