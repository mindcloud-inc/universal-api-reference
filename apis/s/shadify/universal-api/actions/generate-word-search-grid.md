# Shadify: Generate Word Search Grid

Retrieves a random word search grid from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-word-search-grid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-word-search-grid?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-word-search-grid?${params}`, {
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
| `width` | number | no | Optional grid width from 5 to 20. Total cells must not exceed 256. Default is 9. Default: `9`. |
| `height` | number | no | Optional grid height from 5 to 20. Total cells must not exceed 256. Default is 9. Default: `9`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "grid": [
        [
          "string"
        ]
      ],
      "height": 1,
      "width": 1,
      "words": [
        {}
      ],
      "wordsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `grid` | array<array> | Letter grid. |
| `height` | number | Grid height. |
| `width` | number | Grid width. |
| `words` | array<object> | Hidden words and positions. |
| `wordsCount` | number | Number of hidden words. |

## Native endpoint

Through the native Shadify API, this operation is `GET /wordsearch/generator` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-word-search-grid.md) for the provider-specific parameters and requirements.

