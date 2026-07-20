# Craftboxx: Check Assignment Availability

Returns unavailable assignment master data for a date range from Craftboxx.

```
GET https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/check-assignment-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Craftboxx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/check-assignment-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/check-assignment-availability?${params}`, {
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
| `end` | string | no | The interval end timestamp. |
| `exclude` | string | no | Optional assignment ID to exclude from the availability check. |
| `start` | string | no | The interval start timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "employees": [
        {}
      ],
      "tools": [
        {}
      ],
      "vehicles": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `employees` | array<object> | Unavailable employees in the requested interval. |
| `tools` | array<object> | Unavailable tools in the requested interval. |
| `vehicles` | array<object> | Unavailable vehicles in the requested interval. |

## Native endpoint

Through the native Craftboxx API, this operation is `GET assignments/check-availability` (base URL `https://api.craftboxx.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-assignment-availability.md) for the provider-specific parameters and requirements.

