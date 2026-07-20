# Housecall Pro: Get Company



```
GET https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/get-company?${params}`, {
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
      "address": {},
      "defaultArrivalWindow": 1,
      "id": "string",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "serviceAreasData": {},
      "supportEmail": "ava@example.com",
      "timeZone": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `defaultArrivalWindow` | number |  |
| `id` | string |  |
| `logoUrl` | string |  |
| `name` | string |  |
| `phoneNumber` | string |  |
| `serviceAreasData` | object |  |
| `supportEmail` | string |  |
| `timeZone` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Housecall Pro API, this operation is `GET /company` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

