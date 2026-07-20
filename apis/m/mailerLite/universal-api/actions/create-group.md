# MailerLite: Create Group

Creates a new group in MailerLite.

```
POST https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/create-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MC Wizard Stage3 Group"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MC Wizard Stage3 Group"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for the new MailerLite group. Example: `MC Wizard Stage3 Group`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeCount": 1,
      "bouncedCount": 1,
      "clickRate": {
        "float": 1,
        "string": "string"
      },
      "clicksCount": 1,
      "createdAt": "string",
      "id": "string",
      "junkCount": 1,
      "name": "Ava Chen",
      "openRate": {
        "float": 1,
        "string": "string"
      },
      "opensCount": 1,
      "sentCount": 1,
      "unconfirmedCount": 1,
      "unsubscribedCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeCount` | number |  |
| `bouncedCount` | number |  |
| `clickRate.float` | number |  |
| `clickRate.string` | string |  |
| `clicksCount` | number |  |
| `createdAt` | string |  |
| `id` | string |  |
| `junkCount` | number |  |
| `name` | string |  |
| `openRate.float` | number |  |
| `openRate.string` | string |  |
| `opensCount` | number |  |
| `sentCount` | number |  |
| `unconfirmedCount` | number |  |
| `unsubscribedCount` | number |  |

## Native endpoint

Through the native MailerLite API, this operation is `POST /groups` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group.md) for the provider-specific parameters and requirements.

