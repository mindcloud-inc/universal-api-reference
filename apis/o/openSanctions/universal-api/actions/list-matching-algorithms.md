# OpenSanctions: List Matching Algorithms



```
GET https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/list-matching-algorithms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSanctions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/list-matching-algorithms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/list-matching-algorithms?${params}`, {
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
      "algorithms": [
        {}
      ],
      "best": "string",
      "default": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `algorithms` | array<object> | Available matching algorithms. |
| `best` | string | Best/current algorithm name. |
| `default` | string | Default algorithm alias. |

## Native endpoint

Through the native OpenSanctions API, this operation is `GET /algorithms` (base URL `https://api.opensanctions.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-matching-algorithms.md) for the provider-specific parameters and requirements.

