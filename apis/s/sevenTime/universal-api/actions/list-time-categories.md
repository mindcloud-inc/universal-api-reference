# Seven Time: List Time Categories

Retrieves time categories from Seven Time.

```
GET https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-time-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven Time `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-time-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-time-categories?${params}`, {
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
      "articleNumber": "string",
      "color": "string",
      "description": "string",
      "Id": "string",
      "isAbsenceType": true,
      "isActive": true,
      "isInvoiceable": true,
      "isMachineTime": true,
      "isUnsocialHour": true,
      "isVacation": true,
      "isWorkTime": true,
      "name": "Ava Chen",
      "presenceCode": "string",
      "pricePerHour": 1,
      "requirePreAttest": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articleNumber` | string |  |
| `color` | string |  |
| `description` | string |  |
| `Id` | string |  |
| `isAbsenceType` | boolean |  |
| `isActive` | boolean |  |
| `isInvoiceable` | boolean |  |
| `isMachineTime` | boolean |  |
| `isUnsocialHour` | boolean |  |
| `isVacation` | boolean |  |
| `isWorkTime` | boolean |  |
| `name` | string |  |
| `presenceCode` | string |  |
| `pricePerHour` | number |  |
| `requirePreAttest` | boolean |  |

## Native endpoint

Through the native Seven Time API, this operation is `GET /timeCategories` (base URL `https://app.seventime.se/api/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-categories.md) for the provider-specific parameters and requirements.

