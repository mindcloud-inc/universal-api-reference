# Lodgify: Get Rate Calendar

Retrieves a nightly rate calendar from Lodgify.

```
GET https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/get-rate-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lodgify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/get-rate-calendar?connectionId=$CONNECTION_ID&propertyId=779887&roomTypeId=847029&startDate=2026-03-13&endDate=2026-03-20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyId": "779887",
  "roomTypeId": "847029",
  "startDate": "2026-03-13",
  "endDate": "2026-03-20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/get-rate-calendar?${params}`, {
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
| `propertyId` | number | yes | Property identifier from Lodgify. Example: `779887`. |
| `roomTypeId` | number | yes | Room type identifier from Lodgify. Example: `847029`. |
| `startDate` | string | yes | Start date for the rates calendar. Example: `2026-03-13`. |
| `endDate` | string | yes | End date for the rates calendar. Example: `2026-03-20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarItems": [
        {}
      ],
      "rateSettings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarItems` | array<object> |  |
| `rateSettings` | object |  |

## Native endpoint

Through the native Lodgify API, this operation is `GET /v2/rates/calendar` (base URL `https://api.lodgify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rate-calendar.md) for the provider-specific parameters and requirements.

