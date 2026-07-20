# Shipday: List Carriers

Retrieves all available carriers from Shipday.

```
GET https://connect.mindcloud.co/v1/universal/shipday/latest/actions/list-carriers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/list-carriers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipday/latest/actions/list-carriers?${params}`, {
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
      "areaId": 1,
      "carrierPhoto": "string",
      "codeName": "Ava Chen",
      "companyId": 1,
      "email": "ava@example.com",
      "id": 1,
      "isActive": true,
      "isOnShift": true,
      "name": "Ava Chen",
      "personalId": "string",
      "phoneNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `areaId` | number | Area identifier for the carrier. |
| `carrierPhoto` | string | Carrier photo URL. |
| `codeName` | string | Optional code name assigned to the carrier. |
| `companyId` | number | Company identifier for the carrier. |
| `email` | string | Carrier email address. |
| `id` | number | Unique identifier for the carrier. |
| `isActive` | boolean | Whether the carrier is active. |
| `isOnShift` | boolean | Whether the carrier is currently on shift. |
| `name` | string | Full name of the carrier. |
| `personalId` | string | Internal personal ID associated with the carrier. |
| `phoneNumber` | string | Carrier phone number. |

## Native endpoint

Through the native Shipday API, this operation is `GET /carriers` (base URL `https://api.shipday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-carriers.md) for the provider-specific parameters and requirements.

