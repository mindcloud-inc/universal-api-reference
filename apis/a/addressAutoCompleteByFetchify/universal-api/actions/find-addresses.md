# Address Auto-Complete by Fetchify: Find Addresses

Finds address matches in Fetchify by search query.

```
GET https://connect.mindcloud.co/v1/universal/addressAutoCompleteByFetchify/latest/actions/find-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Address Auto-Complete by Fetchify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressAutoCompleteByFetchify/latest/actions/find-addresses?connectionId=$CONNECTION_ID&query=string&country=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string",
  "country": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressAutoCompleteByFetchify/latest/actions/find-addresses?${params}`, {
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
| `query` | string | yes | The partial address or postcode to autocomplete. |
| `country` | string | yes | Three-letter Fetchify country code such as `gbr` or `usa`. |
| `id` | string | no | Optional grouping identifier returned by a previous find call. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extra.bestMatchOnly` | boolean | no | Return only the top autocomplete match. |
| `extra.noGroupings` | boolean | no | Disable grouped results in the autocomplete response. |
| `extra.excludePobox` | boolean | no | Exclude PO box style matches. |
| `extra.excludeAreas` | list<string> | no | Optional list of areas to exclude from autocomplete results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "count": 1,
          "id": "string",
          "labels": [
            "string"
          ]
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
| `results[].count` | number |  |
| `results[].id` | string |  |
| `results[].labels[]` | string |  |

## Native endpoint

Through the native Address Auto-Complete by Fetchify API, this operation is `GET /find` (base URL `https://api.craftyclicks.co.uk/address/1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-addresses.md) for the provider-specific parameters and requirements.

