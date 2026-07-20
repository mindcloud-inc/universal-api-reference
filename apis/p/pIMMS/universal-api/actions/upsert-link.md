# PIMMS: Upsert Link

Updates an existing deep link in PIMMS, or creates one.

```
PUT https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/upsert-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PIMMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/upsert-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/upsert-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Destination URL the deep link redirects to. Supports standard webpages and in-app routing for mobile apps. |
| `domain` | string | no | Custom domain for your branded deep link. Defaults to the workspace’s primary domain or 'pim.ms'. |
| `key` | string | no | Custom slug for the short URL. If omitted, an automatic 7-character key is generated. |
| `externalId` | string | no | External identifier for syncing link data with your internal CRM or analytics tools. Passed in query parameters prefixed by 'ext_'. |
| `prefix` | string | no | Custom URL path prefix for grouping auto-generated slugs (e.g., '/promo/' resulting in '/promo/abc123'). Ignored if 'key' is specified. |
| `trackConversion` | boolean | no | Enable detailed conversion tracking to attribute actions like signups or purchases directly to this link. |
| `archived` | boolean | no | Archive the link to hide it from primary analytics while keeping it active for redirects. |
| `tagIds` | string | no | List of existing tag IDs to categorize and filter links by campaigns, audiences, or purposes. |
| `tagNames` | string | no | New or existing tag names to assign for improved readability and organization. |
| `comments` | string | no | Internal notes for team members about link context, purpose, or specific campaign details. |
| `expiresAt` | string | no | ISO 8601 timestamp when the link should stop redirecting users. |
| `expiredUrl` | string | no | Fallback destination URL after link expiration, preventing broken user experiences. |
| `title` | string | no | Custom Open Graph (OG) title to optimize social media sharing and improve link previews. |
| `description` | string | no | Custom Open Graph description for better engagement when shared on social platforms. |
| `image` | string | no | URL for a custom OG image to enhance visual appeal and click-through rates on social media. |
| `video` | string | no | Custom video URL for rich media previews via Open Graph when sharing links. |
| `ios` | string | no | The iOS destination URL for the short link for iOS device targeting. |
| `android` | string | no | The Android destination URL for the short link for Android device targeting. |
| `doIndex` | boolean | no | Allow search engine indexing of the deep link. Defaults to false for privacy. |
| `utmSource` | string | no | UTM source parameter for tracking the origin of traffic (e.g., 'linkedin', 'facebook', 'newsletter'). |
| `utmMedium` | string | no | UTM medium parameter identifying traffic medium such as 'post', 'email', 'social', or 'cpc'. |
| `utmCampaign` | string | no | UTM campaign parameter for tracking specific marketing initiatives or promotions. |
| `utmTerm` | string | no | UTM term parameter for keyword analysis, often used in paid search campaigns. |
| `utmContent` | string | no | UTM content parameter distinguishing different content variations or link placements within a campaign. |
| `ref` | string | no | Custom referral parameter appended as '?ref=' for downstream attribution and analysis. |
| `webhookIds[]` | array<string> | no | Webhook IDs to trigger real-time notifications upon link clicks, ideal for integrating with analytics or marketing automation tools. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "android": "string",
      "archived": true,
      "clicks": 1,
      "comments": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "domain": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "image": "string",
      "ios": "string",
      "key": "string",
      "lastClicked": "string",
      "leads": 1,
      "qrCode": "string",
      "shortLink": "https://example.com",
      "tags": [
        {}
      ],
      "title": "string",
      "trackConversion": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": "string",
      "utm_campaign": "string",
      "utm_content": "string",
      "utm_medium": "string",
      "utm_source": "string",
      "utm_term": "string",
      "video": "string",
      "webhookIds": [
        "string"
      ],
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `android` | string | The Android destination URL for the short link for Android device targeting. |
| `archived` | boolean | Determines if the link is archived, thus excluded from standard analytics views. |
| `clicks` | number | Total click count tracking user engagements. |
| `comments` | string | Internal team notes describing the context, strategy, or use of the link. |
| `createdAt` | date | Timestamp when the link was first created. |
| `description` | string | OG description for enhanced social previews, either automatically fetched or manually customized. |
| `domain` | string | Domain used for the deep link, e.g., 'yourbrand.com' or 'pim.ms'. |
| `expiresAt` | date | Expiration timestamp in ISO 8601 format; after this, the link redirects to an expired URL or returns a 404. |
| `id` | string | Unique internal identifier for the deep link. |
| `image` | string | URL to the OG image displayed in social previews, improving shareability. |
| `ios` | string | The iOS destination URL for the short link for iOS device targeting. |
| `key` | string | Short URL slug appended after the domain, uniquely identifying the link. |
| `lastClicked` | string | Timestamp of the most recent click event. |
| `leads` | number | Total conversions attributed directly to this link. |
| `qrCode` | string | Direct link to the dynamically generated QR code for offline or print campaigns. |
| `shortLink` | string | Fully constructed deep link URL including domain and protocol. |
| `tags` | array<object> | Associated tags for organizing links by campaigns, audiences, or other criteria. |
| `title` | string | OG title for optimized social media link previews, fetched or set manually. |
| `trackConversion` | boolean | Indicates whether this link actively tracks conversion events like leads or sales. |
| `updatedAt` | date | Timestamp when the link was last modified. |
| `url` | string | Complete original destination URL or mobile app route to which the link redirects users. |
| `userId` | string | Identifier of the user who created the link. |
| `utm_campaign` | string | Assigned UTM campaign for detailed campaign-level tracking. |
| `utm_content` | string | Assigned UTM content for distinguishing content variations within the same campaign. |
| `utm_medium` | string | Assigned UTM medium for categorizing the traffic source. |
| `utm_source` | string | Assigned UTM source parameter for tracking marketing origins. |
| `utm_term` | string | Assigned UTM term parameter used for keyword or search tracking. |
| `video` | string | Optional video URL used in rich media previews via Open Graph. |
| `webhookIds` | array<string> | Webhooks triggered on each click event for real-time tracking and integration purposes. |
| `workspaceId` | string | Identifier of the workspace that the link belongs to. |

## Native endpoint

Through the native PIMMS API, this operation is `PUT /links/upsert` (base URL `https://api.pimms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-link.md) for the provider-specific parameters and requirements.

