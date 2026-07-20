# DivvyHQ: Patch Allowed Content Type In Calendar



```
PUT https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/patch-allowed-content-type-in-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DivvyHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/patch-allowed-content-type-in-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/patch-allowed-content-type-in-calendar', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendar": 1,
      "contentType": {},
      "enabled": true,
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendar` | number | The linked calendar id. |
| `contentType` | object | The nested content type definition. |
| `enabled` | boolean | Whether the content type is enabled. |
| `id` | number | The allowed content type row id. |

## Native endpoint

Through the native DivvyHQ API, this operation is `PATCH /allowedctypeincalendars/:id/` (base URL `https://app.divvyhq.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-allowed-content-type-in-calendar.md) for the provider-specific parameters and requirements.

