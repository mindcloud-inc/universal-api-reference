# LightwaveRF Heating: List Structures

Retrieves account structures from LightwaveRF Heating.

```
GET https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/list-structures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Heating `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/list-structures?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/list-structures?${params}`, {
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
      "structures": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `structures` | array<object> | Available LightwaveRF structures. |

## Native endpoint

Through the native LightwaveRF Heating API, this operation is `GET /v1/structures` (base URL `https://publicapi.lightwaverf.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-structures.md) for the provider-specific parameters and requirements.

