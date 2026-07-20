# Segmind: Delete Dedicated Endpoint



```
DELETE https://connect.mindcloud.co/v1/universal/segmind/latest/actions/delete-dedicated-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Segmind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/segmind/latest/actions/delete-dedicated-endpoint?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/segmind/latest/actions/delete-dedicated-endpoint?${params}`, {
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
      "endpointId": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpointId` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Segmind API, this operation is `POST https://api.spotprod.segmind.com/endpoint/delete` (base URL `https://api.segmind.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-dedicated-endpoint.md) for the provider-specific parameters and requirements.

