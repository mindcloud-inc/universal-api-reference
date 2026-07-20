# PickFu: Get Reporting Traits



```
GET https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/get-reporting-traits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PickFu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/get-reporting-traits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/get-reporting-traits?${params}`, {
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
      "permalink": "https://example.com",
      "trait_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permalink` | string | Stable PickFu reporting trait permalink token. |
| `trait_name` | string | Human-readable PickFu reporting trait label. |

## Native endpoint

Through the native PickFu API, this operation is `GET /traits/reporting` (base URL `https://api.pickfu.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reporting-traits.md) for the provider-specific parameters and requirements.

