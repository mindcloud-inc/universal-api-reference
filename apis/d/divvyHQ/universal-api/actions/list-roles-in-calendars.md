# DivvyHQ: List Roles In Calendars



```
GET https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/list-roles-in-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DivvyHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/list-roles-in-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/list-roles-in-calendars?${params}`, {
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
      "calendar": 1,
      "id": 1,
      "member": 1,
      "role": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendar` | number | The linked calendar id. |
| `id` | number | The role-in-calendar id. |
| `member` | number | The linked member id. |
| `role` | number | The role id. |

## Native endpoint

Through the native DivvyHQ API, this operation is `GET /roleincalendars/` (base URL `https://app.divvyhq.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-roles-in-calendars.md) for the provider-specific parameters and requirements.

