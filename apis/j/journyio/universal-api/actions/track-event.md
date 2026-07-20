# Journy.io: Track Event



```
POST https://connect.mindcloud.co/v1/universal/journyio/latest/actions/track-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Journy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/journyio/latest/actions/track-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/journyio/latest/actions/track-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identification.account.accountId` | string | no | Unique identifier for the account in your database. |
| `identification.account.domain` | string | no | The domain associated with the account. |
| `identification.user.email` | string | no | Email address of the user. |
| `identification.user.userId` | string | no | Unique identifier for the user in your database. |
| `metadata` | object | no | Optional event metadata. |
| `name` | string | yes | Name of the event to track. |
| `triggeredAt` | date | no | Datetime when the event happened. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "meta": {
        "requestId": "string",
        "status": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `meta.requestId` | string |  |
| `meta.status` | number |  |

## Native endpoint

Through the native Journy.io API, this operation is `POST /track` (base URL `https://api.journy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-event.md) for the provider-specific parameters and requirements.

