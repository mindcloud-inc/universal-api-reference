# Sipuni: List Operators

Retrieves operators and presence statuses from Sipuni.

```
GET https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/list-operators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sipuni `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/list-operators?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/list-operators?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw CSV response returned by Sipuni. |

## Native endpoint

Through the native Sipuni API, this operation is `GET /statistic/operators` (base URL `https://sipuni.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-operators.md) for the provider-specific parameters and requirements.

