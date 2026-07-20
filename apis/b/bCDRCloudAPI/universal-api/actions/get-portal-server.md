# BCDR Cloud: Get Portal Server



```
GET https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-portal-server
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BCDR Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-portal-server?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-portal-server?${params}`, {
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
      "item0": "string",
      "item1": "string",
      "item2": "string",
      "item3": 1,
      "item4": 1,
      "item5": 1,
      "item6": 1,
      "item7": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item0` | string | First positional value returned by the portal server endpoint. |
| `item1` | string | Second positional value returned by the portal server endpoint. |
| `item2` | string | Third positional value returned by the portal server endpoint. |
| `item3` | number | Fourth positional value returned by the portal server endpoint. |
| `item4` | number | Fifth positional value returned by the portal server endpoint. |
| `item5` | number | Sixth positional value returned by the portal server endpoint. |
| `item6` | number | Seventh positional value returned by the portal server endpoint. |
| `item7` | string | Eighth positional value returned by the portal server endpoint. |

## Native endpoint

Through the native BCDR Cloud API, this operation is `POST /portal_server` (base URL `https://console1.bdrshield.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-portal-server.md) for the provider-specific parameters and requirements.

