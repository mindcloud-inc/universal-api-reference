# Yay.com: Get Next Hunt Group Extension

Retrieves the next hunt group extension from Yay.com.

```
GET https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/get-next-hunt-group-extension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yay.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/get-next-hunt-group-extension?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/get-next-hunt-group-extension?${params}`, {
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
      "nextExtension": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextExtension` | number |  |

## Native endpoint

Through the native Yay.com API, this operation is `GET /voip/next-extension/group` (base URL `https://api.yay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-next-hunt-group-extension.md) for the provider-specific parameters and requirements.

