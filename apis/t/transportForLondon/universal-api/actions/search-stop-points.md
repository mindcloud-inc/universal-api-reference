# Transport for London: Search Stop Points

Finds stop points in Transport for London by name or code.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/search-stop-points
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/search-stop-points?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/search-stop-points?${params}`, {
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
| `query` | string | yes | Stop point search text, common name, or 5-digit Countdown bus stop code. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modes` | string | no | Optional comma-separated modes to filter stop point search. |
| `maxResults` | number | no | Optional maximum number of search results. TfL defaults to and caps this at 50. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "matches": [
        {}
      ],
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
| `query` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /StopPoint/Search/:query` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-stop-points.md) for the provider-specific parameters and requirements.

