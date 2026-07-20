# Planday: List Shift Types

Retrieves a list of shift types from Planday.

```
GET https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-shift-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-shift-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-shift-types?${params}`, {
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
| `isActive` | boolean | no |  |
| `limit` | number | no |  |
| `offset` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowBooking": true,
      "allowsBreaks": true,
      "color": "string",
      "id": 1,
      "includeInSchedulePrint": true,
      "isActive": true,
      "name": "Ava Chen",
      "paymentType": "string",
      "payPercentage": 1,
      "salaryCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowBooking` | boolean |  |
| `allowsBreaks` | boolean |  |
| `color` | string |  |
| `id` | number |  |
| `includeInSchedulePrint` | boolean |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `paymentType` | string |  |
| `payPercentage` | number |  |
| `salaryCode` | string |  |

## Native endpoint

Through the native Planday API, this operation is `GET /scheduling/v1.0/shifttypes` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-shift-types.md) for the provider-specific parameters and requirements.

