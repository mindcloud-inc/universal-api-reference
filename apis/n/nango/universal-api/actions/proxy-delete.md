# Nango: Proxy DELETE



```
DELETE https://connect.mindcloud.co/v1/universal/nango/latest/actions/proxy-delete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nango `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nango/latest/actions/proxy-delete?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nango/latest/actions/proxy-delete?${params}`, {
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
      "data": {},
      "headers": {},
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `headers` | object |  |
| `statusCode` | number |  |

## Native endpoint

Through the native Nango API, this operation is `DELETE /proxy/:anyPath` (base URL `https://api.nango.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/proxy-delete.md) for the provider-specific parameters and requirements.

