# Mekari Qontak: List Deal Full Fields

Retrieves all full deal fields from Mekari Qontak.

```
GET https://connect.mindcloud.co/v1/universal/mekariQontak/latest/actions/get-all-deal-full-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mekari Qontak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mekariQontak/latest/actions/get-all-deal-full-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mekariQontak/latest/actions/get-all-deal-full-fields?${params}`, {
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
      "meta": {
        "developerMessage": "string",
        "errorCode": "string",
        "info": "string",
        "message": "string",
        "status": 1,
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object |  |
| `meta.developerMessage` | string |  |
| `meta.errorCode` | string |  |
| `meta.info` | string |  |
| `meta.message` | string |  |
| `meta.status` | number |  |
| `meta.type` | string |  |

## Native endpoint

Through the native Mekari Qontak API, this operation is `GET qontak/crm/deals/full-fields` (base URL `https://api.mekari.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-deal-full-fields.md) for the provider-specific parameters and requirements.

