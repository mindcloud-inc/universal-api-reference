# Aloware: Clear User Power Dialer Lists

Clears all contacts from an Aloware user's power dialer lists.

```
PUT https://connect.mindcloud.co/v1/universal/aloware/latest/actions/clear-user-power-dialer-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aloware `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/clear-user-power-dialer-lists" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aloware/latest/actions/clear-user-power-dialer-lists', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | User whose power dialer lists you want to clear. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider success message when the user's power dialer lists clearing process is initiated. |

## Native endpoint

Through the native Aloware API, this operation is `POST /api/v1/webhook/powerdialer-clear-user-lists` (base URL `https://app.aloware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-user-power-dialer-lists.md) for the provider-specific parameters and requirements.

