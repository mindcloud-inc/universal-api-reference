# PBX Yeastar: Query PBX Information

Retrieves PBX information from PBX Yeastar.

```
GET https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-pbx-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PBX Yeastar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-pbx-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-pbx-information?${params}`, {
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
      "errcode": 1,
      "errmsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | PBX information. |
| `errcode` | number | Yeastar result code. 0 means success. |
| `errmsg` | string | Yeastar result message. |

## Native endpoint

Through the native PBX Yeastar API, this operation is `GET /system/information` (base URL `{{credentials.baseUrl}}/openapi/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-pbx-information.md) for the provider-specific parameters and requirements.

