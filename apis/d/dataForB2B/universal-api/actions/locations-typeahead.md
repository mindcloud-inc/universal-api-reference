# DataForB2B: Locations Typeahead

Retrieves location suggestions from DataForB2B.

```
GET https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/locations-typeahead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForB2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/locations-typeahead?connectionId=$CONNECTION_ID&q=new%20york" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "new york"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/locations-typeahead?${params}`, {
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
| `q` | string | yes | Autocomplete query string. Default: `new york`. |
| `limit` | number | no | Maximum number of suggestions to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
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
| `results` | array<object> |  |

## Native endpoint

Through the native DataForB2B API, this operation is `GET /typeahead/locations` (base URL `https://api.dataforb2b.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/locations-typeahead.md) for the provider-specific parameters and requirements.

