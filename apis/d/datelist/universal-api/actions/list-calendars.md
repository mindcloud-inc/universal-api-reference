# Datelist: List Calendars

Retrieves available calendars from your Datelist account.

```
GET https://connect.mindcloud.co/v1/universal/datelist/latest/actions/list-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datelist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datelist/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datelist/latest/actions/list-calendars?${params}`, {
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
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Calendar ID. |
| `name` | string | Calendar name. |

## Native endpoint

Through the native Datelist API, this operation is `GET /calendars` (base URL `https://datelist.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendars.md) for the provider-specific parameters and requirements.

