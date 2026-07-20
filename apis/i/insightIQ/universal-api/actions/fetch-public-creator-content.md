# InsightIQ: Fetch Public Creator Content

Retrieves public creator content from InsightIQ.

```
GET https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/fetch-public-creator-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/fetch-public-creator-content?connectionId=$CONNECTION_ID&profileUrl=https%3A%2F%2Fexample.com&workPlatformId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileUrl": "https://example.com",
  "workPlatformId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/fetch-public-creator-content?${params}`, {
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
| `contentType` | string | no | Content type filter for profile content fetches Default: `REELS`. |
| `offset` | number | no | Sequential offset for profile content pagination Default: `0`. |
| `profileUrl` | string | yes | Public profile URL to fetch content from |
| `workPlatformId` | string | yes | Work platform ID for the profile |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "metadata": {},
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `metadata` | object |  |
| `updated_at` | date |  |

## Native endpoint

Through the native InsightIQ API, this operation is `POST /v1/social/creators/contents/fetch` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-public-creator-content.md) for the provider-specific parameters and requirements.

