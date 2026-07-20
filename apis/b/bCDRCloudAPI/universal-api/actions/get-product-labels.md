# BCDR Cloud: Get Product Labels



```
GET https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-product-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BCDR Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-product-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-product-labels?${params}`, {
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
      "ReplaceKeys": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ReplaceKeys` | object | Product-label replacement map returned by the endpoint. |

## Native endpoint

Through the native BCDR Cloud API, this operation is `POST /get_prod_labels` (base URL `https://console1.bdrshield.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-labels.md) for the provider-specific parameters and requirements.

