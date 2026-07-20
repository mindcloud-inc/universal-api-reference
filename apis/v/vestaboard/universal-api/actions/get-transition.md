# Vestaboard: Get Transition

Retrieves transition settings from Vestaboard.

```
GET https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/get-transition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vestaboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/get-transition?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/get-transition?${params}`, {
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
      "transition": "string",
      "transitionSpeed": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `transition` | string | Current transition style for the device. |
| `transitionSpeed` | string | Current transition speed for the device. |

## Native endpoint

Through the native Vestaboard API, this operation is `GET /transition` (base URL `https://cloud.vestaboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transition.md) for the provider-specific parameters and requirements.

