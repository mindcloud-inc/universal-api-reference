# Cursion: List Tests

Retrieves a list of tests from Cursion.

```
GET https://connect.mindcloud.co/v1/universal/cursion/latest/actions/list-tests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/list-tests?connectionId=$CONNECTION_ID&limit=25&offset=0&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursion/latest/actions/list-tests?${params}`, {
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
| `pageId` | string | yes | The page ID to list tests for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
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
| `count` | number |  |
| `next` | string |  |
| `previous` | string |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Cursion API, this operation is `GET /test` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tests.md) for the provider-specific parameters and requirements.

