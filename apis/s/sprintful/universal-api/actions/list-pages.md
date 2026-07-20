# Sprintful: List Pages

Retrieves booking pages available in Sprintful.

```
GET https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/list-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sprintful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/list-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/list-pages?${params}`, {
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
      "data": {
        "bookingsCount": 1,
        "name": "Ava Chen",
        "slug": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Booking pages available in Sprintful. |
| `data.bookingsCount` | number | Number of bookings associated with the page. |
| `data.name` | string | The booking page name. |
| `data.slug` | string | The booking page slug. |
| `success` | boolean | Whether the Sprintful request succeeded. |

## Native endpoint

Through the native Sprintful API, this operation is `GET /pages` (base URL `https://app.sprintful.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pages.md) for the provider-specific parameters and requirements.

