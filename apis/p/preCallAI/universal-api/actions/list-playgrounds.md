# PreCallAI: List Playgrounds

Retrieves playground history from PreCallAI.

```
GET https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-playgrounds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PreCallAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-playgrounds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-playgrounds?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "message": "string",
      "status": 1,
      "success": true,
      "totalItems": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of playground calls returned by PreCallAI. |
| `message` | string | Provider status message for listing playground calls. |
| `status` | number | HTTP-style status returned by PreCallAI. |
| `success` | boolean | Whether the playground list request succeeded. |
| `totalItems` | number | Total playground calls returned. |
| `totalPages` | number | Total pages available for playground calls. |

## Native endpoint

Through the native PreCallAI API, this operation is `GET /playground/list` (base URL `https://api.precallai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-playgrounds.md) for the provider-specific parameters and requirements.

