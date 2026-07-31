# Where the ISS at: List Satellites



```
GET https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/list-satellites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Where the ISS at `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/list-satellites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/list-satellites?${params}`, {
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
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | NORAD catalog ID. |
| `name` | string | Satellite common name. |

## Native endpoint

Through the native Where the ISS at API, this operation is `GET /satellites` (base URL `https://api.wheretheiss.at/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-satellites.md) for the provider-specific parameters and requirements.

