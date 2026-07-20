# DataForB2B: Search People

Searches for people in DataForB2B.

```
GET https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/search-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForB2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/search-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/search-people?${params}`, {
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
| `filters` | object | no | JSON filter object using DataForB2B search conditions. Default: `{}`. |
| `count` | number | no | Maximum number of results to return. Default: `1`. |
| `offset` | number | no | Result offset for pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "credits_used": 1,
      "offset": 1,
      "results": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `credits_used` | number |  |
| `offset` | number |  |
| `results` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native DataForB2B API, this operation is `POST /search/people` (base URL `https://api.dataforb2b.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-people.md) for the provider-specific parameters and requirements.

