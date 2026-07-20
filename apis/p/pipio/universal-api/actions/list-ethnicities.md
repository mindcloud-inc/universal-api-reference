# Pipio: List Ethnicities

Finds supported avatar ethnicities in Pipio.

```
GET https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-ethnicities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-ethnicities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-ethnicities?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Ethnicity value. |

## Native endpoint

Through the native Pipio API, this operation is `GET /actor/ethnicities/all` (base URL `https://avatar.pipio.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ethnicities.md) for the provider-specific parameters and requirements.

