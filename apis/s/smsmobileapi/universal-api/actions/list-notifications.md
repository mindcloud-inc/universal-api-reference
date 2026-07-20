# Smsmobileapi: List Notifications

Retrieves notifications from Smsmobileapi.

```
GET https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smsmobileapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-notifications?${params}`, {
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
| `sidentifiant` | string | no | Filter notifications by the target mobile identifier. |
| `distribued` | list | no | Limit results to distributed or not-distributed notifications. One of: `0`, `1`. |
| `date_from` | date | no | Only include notifications sent from this date forward. |
| `date_to` | date | no | Only include notifications sent up to this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {}
      ],
      "filters": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of rows returned in data. |
| `data` | array<object> | Notification rows returned by the provider. |
| `filters` | object | Echoed filter values applied to the request. |
| `message` | string | Provider status message for the request. |
| `success` | boolean | Whether the notification lookup succeeded. |

## Native endpoint

Through the native Smsmobileapi API, this operation is `GET /notification/list/` (base URL `https://api.smsmobileapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notifications.md) for the provider-specific parameters and requirements.

