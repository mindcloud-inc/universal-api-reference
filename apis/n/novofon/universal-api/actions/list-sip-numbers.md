# Novofon: List SIP Numbers

Retrieves SIP numbers from Novofon.

```
GET https://connect.mindcloud.co/v1/universal/novofon/latest/actions/list-sip-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novofon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/list-sip-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novofon/latest/actions/list-sip-numbers?${params}`, {
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
      "left": 1,
      "sips": [
        {
          "displayName": "Ava Chen",
          "id": "string",
          "lines": 1
        }
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
| `left` | number |  |
| `sips[].displayName` | string |  |
| `sips[].id` | string |  |
| `sips[].lines` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Novofon API, this operation is `GET /v1/sip/` (base URL `https://api.novofon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sip-numbers.md) for the provider-specific parameters and requirements.

