# HR Partner: List Assets



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-assets?${params}`, {
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
      "assetIdentifier": "string",
      "assetType": "string",
      "description": "string",
      "employee": {},
      "id": 1,
      "inDate": "2026-05-07T12:00:00.000Z",
      "outDate": "2026-05-07T12:00:00.000Z",
      "serialNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetIdentifier` | string |  |
| `assetType` | string |  |
| `description` | string |  |
| `employee` | object |  |
| `id` | number |  |
| `inDate` | date |  |
| `outDate` | date |  |
| `serialNumber` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /assets` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

