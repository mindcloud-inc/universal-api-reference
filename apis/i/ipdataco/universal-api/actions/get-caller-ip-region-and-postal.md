# ipdata.co: Get Caller IP Region And Postal



```
GET https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-region-and-postal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ipdata.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-region-and-postal?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-region-and-postal?${params}`, {
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
      "city": "string",
      "postal": "string",
      "region": "string",
      "region_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `postal` | string |  |
| `region` | string |  |
| `region_code` | string |  |

## Native endpoint

Through the native ipdata.co API, this operation is `GET /` (base URL `https://api.ipdata.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-caller-ip-region-and-postal.md) for the provider-specific parameters and requirements.

