# PPM Express: List Ideas



```
GET https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/list-ideas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PPM Express `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/list-ideas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/list-ideas?${params}`, {
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
      "data": [
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
| `data` | array<object> | The ideas in the tenant. |

## Native endpoint

Through the native PPM Express API, this operation is `GET /@:tenantName/v1.0/ideas` (base URL `https://api-us.ppm.express`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ideas.md) for the provider-specific parameters and requirements.

