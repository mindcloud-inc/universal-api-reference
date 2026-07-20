# ConvertHub: Get All Supported Conversions

Retrieves all supported conversion mappings from ConvertHub.

```
GET https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-all-supported-conversions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-all-supported-conversions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-all-supported-conversions?${params}`, {
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
      "conversion_map": {},
      "formats": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversion_map` | object |  |
| `formats` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native ConvertHub API, this operation is `GET /v2/formats/supported-conversions` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-supported-conversions.md) for the provider-specific parameters and requirements.

