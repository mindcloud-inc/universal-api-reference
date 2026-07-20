# Electricity Maps: List Data Centers



```
GET https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/list-data-centers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Electricity Maps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/list-data-centers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/list-data-centers?${params}`, {
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
      "displayName": "Ava Chen",
      "lonlat": [
        1
      ],
      "operationalSince": "string",
      "provider": "string",
      "region": "string",
      "source": "string",
      "status": "string",
      "zoneKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `lonlat` | array<number> |  |
| `operationalSince` | string |  |
| `provider` | string |  |
| `region` | string |  |
| `source` | string |  |
| `status` | string |  |
| `zoneKey` | string |  |

## Native endpoint

Through the native Electricity Maps API, this operation is `GET /data-centers` (base URL `https://api.electricitymaps.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-centers.md) for the provider-specific parameters and requirements.

