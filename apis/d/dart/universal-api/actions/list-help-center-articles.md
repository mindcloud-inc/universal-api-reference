# Dart: List Help Center Articles

Retrieves help center articles from Dart.

```
GET https://connect.mindcloud.co/v1/universal/dart/latest/actions/list-help-center-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dart/latest/actions/list-help-center-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dart/latest/actions/list-help-center-articles?${params}`, {
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
| `query` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "description": "string",
          "title": "string",
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
| `items[].description` | string |  |
| `items[].title` | string |  |
| `items[].url` | string |  |

## Native endpoint

Through the native Dart API, this operation is `GET /help-center-articles/list` (base URL `https://app.dartai.com/api/v0/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-help-center-articles.md) for the provider-specific parameters and requirements.

