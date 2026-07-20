# Transport for London: Search TfL

Finds site results in Transport for London by query.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/search-tfl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/search-tfl?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/search-tfl?${params}`, {
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
| `query` | string | yes | Site search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "matches": [
        {}
      ],
      "maxScore": 1,
      "pageSize": 1,
      "query": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `matches` | array<object> |  |
| `maxScore` | number |  |
| `pageSize` | number |  |
| `query` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /Search` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tfl.md) for the provider-specific parameters and requirements.

