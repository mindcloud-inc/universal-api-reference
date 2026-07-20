# Responsr: List Variables



```
GET https://connect.mindcloud.co/v1/universal/responsr/latest/actions/list-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Responsr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/responsr/latest/actions/list-variables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/responsr/latest/actions/list-variables?${params}`, {
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
      "customerContextId": 1,
      "keyVariableId": 1,
      "list": [
        {}
      ],
      "pagingInfo": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerContextId` | number |  |
| `keyVariableId` | number |  |
| `list` | array<object> |  |
| `pagingInfo` | object |  |

## Native endpoint

Through the native Responsr API, this operation is `GET /api/v1.0/variables` (base URL `https://app.responsr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-variables.md) for the provider-specific parameters and requirements.

