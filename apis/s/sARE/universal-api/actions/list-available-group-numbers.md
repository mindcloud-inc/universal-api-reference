# SARE: List Available Group Numbers

Lists available group numbers in SARE.

```
GET https://connect.mindcloud.co/v1/universal/sARE/latest/actions/list-available-group-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SARE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sARE/latest/actions/list-available-group-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sARE/latest/actions/list-available-group-numbers?${params}`, {
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
      "code": 1,
      "response": [
        1
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | HTTP-like response code returned by the SARE API. |
| `response` | array<number> | Available SARE group numbers for the connected account. |
| `status` | string | Status text returned by the SARE API. |

## Native endpoint

Through the native SARE API, this operation is `GET /group/free` (base URL `https://s.enewsletter.pl/api/v1/{{credentials.uid}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-group-numbers.md) for the provider-specific parameters and requirements.

