# SendBox: List Saved Addresses



```
GET https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/list-saved-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/list-saved-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/list-saved-addresses?${params}`, {
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
| `page` | number | no | Page number to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "filter_by": {},
      "page_by": {},
      "query": "string",
      "results": [
        {}
      ],
      "sort_by": [
        {}
      ],
      "view": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `filter_by` | object |  |
| `page_by` | object |  |
| `query` | string |  |
| `results` | array<object> |  |
| `sort_by` | array<object> |  |
| `view` | string |  |

## Native endpoint

Through the native SendBox API, this operation is `GET /auth/addresses` (base URL `https://live.sendbox.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-saved-addresses.md) for the provider-specific parameters and requirements.

