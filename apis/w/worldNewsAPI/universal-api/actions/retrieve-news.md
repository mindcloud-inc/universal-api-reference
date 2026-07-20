# World News API: Retrieve News

Retrieves news articles from World News API by ID.

```
GET https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/retrieve-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/retrieve-news?connectionId=$CONNECTION_ID&ids=422590668" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "422590668"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/retrieve-news?${params}`, {
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
| `ids` | string | yes | Comma-separated list of World News API article ids to retrieve. Accepts multiple values in one string, delimited by `,`. Default: `422590668`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "news": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `news` | array<object> | News articles returned for the requested article ids. |

## Native endpoint

Through the native World News API API, this operation is `GET /retrieve-news` (base URL `https://api.worldnewsapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-news.md) for the provider-specific parameters and requirements.

