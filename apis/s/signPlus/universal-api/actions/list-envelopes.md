# Sign.Plus: List Envelopes



```
GET https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/list-envelopes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign.Plus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/list-envelopes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/list-envelopes?${params}`, {
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
      "envelopes": [
        {}
      ],
      "has_next_page": true,
      "has_previous_page": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `envelopes` | array<object> |  |
| `has_next_page` | boolean |  |
| `has_previous_page` | boolean |  |

## Native endpoint

Through the native Sign.Plus API, this operation is `POST /envelopes` (base URL `https://restapi.sign.plus/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-envelopes.md) for the provider-specific parameters and requirements.

