# Beds24: List Room Calendar

Retrieves room calendar values from Beds24.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-room-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-room-calendar?connectionId=$CONNECTION_ID&endDate=string&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "string",
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-room-calendar?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endDate` | string | yes | Calendar range end date in YYYY-MM-DD format. |
| `startDate` | string | yes | Calendar range start date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendar": {},
      "propertyId": 1,
      "roomId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendar` | object |  |
| `propertyId` | number |  |
| `roomId` | number |  |

## Native endpoint

Through the native Beds24 API, this operation is `GET /inventory/rooms/calendar` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-room-calendar.md) for the provider-specific parameters and requirements.

