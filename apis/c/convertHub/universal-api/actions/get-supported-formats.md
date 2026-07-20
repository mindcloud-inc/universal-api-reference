# ConvertHub: Get Supported Formats

Retrieves supported file formats from ConvertHub.

```
GET https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-supported-formats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-supported-formats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-supported-formats?${params}`, {
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
      "formats": {},
      "success": true,
      "total_formats": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formats` | object |  |
| `success` | boolean |  |
| `total_formats` | number |  |

## Native endpoint

Through the native ConvertHub API, this operation is `GET /v2/formats` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supported-formats.md) for the provider-specific parameters and requirements.

