# Lasso X: List Paqle News

Retrieves Paqle news for a Lasso X entity.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-paqle-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-paqle-news?connectionId=$CONNECTION_ID&lasso_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lasso_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-paqle-news?${params}`, {
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
| `lasso_id` | string | yes | Lasso ID, for example CVR-1-34580820. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "continuationToken": "string",
      "news": [
        {
          "content": "string",
          "headline": "string",
          "lassoIds": [
            "string"
          ],
          "promotedUntil": "2026-05-07T12:00:00.000Z",
          "provider": "string",
          "providerData": {
            "extract": [
              {
                "text": "string"
              }
            ],
            "headline": [
              {
                "text": "string"
              }
            ],
            "paqleUrl": "https://example.com",
            "published": "2026-05-07T12:00:00.000Z",
            "sourceName": "Ava Chen",
            "url": "https://example.com"
          },
          "storyId": "string",
          "time": "2026-05-07T12:00:00.000Z",
          "type": "string",
          "uniqueId": "string",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `continuationToken` | string |  |
| `news[].content` | string |  |
| `news[].headline` | string |  |
| `news[].lassoIds[]` | string |  |
| `news[].promotedUntil` | date |  |
| `news[].provider` | string |  |
| `news[].providerData.extract[].text` | string |  |
| `news[].providerData.headline[].text` | string |  |
| `news[].providerData.paqleUrl` | string |  |
| `news[].providerData.published` | date |  |
| `news[].providerData.sourceName` | string |  |
| `news[].providerData.url` | string |  |
| `news[].storyId` | string |  |
| `news[].time` | date |  |
| `news[].type` | string |  |
| `news[].uniqueId` | string |  |
| `news[].url` | string |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /data/paqle/:lassoId/news` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-paqle-news.md) for the provider-specific parameters and requirements.

