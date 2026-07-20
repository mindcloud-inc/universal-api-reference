# CreateSend: Add Subscriber

Creates a new subscriber in CreateSend.

```
POST https://connect.mindcloud.co/v1/universal/createSend/latest/actions/add-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CreateSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/createSend/latest/actions/add-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "c9026d1f12bd6b3e41844e3257f4d603",
  "emailAddress": "codex-stage4-default@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/createSend/latest/actions/add-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "c9026d1f12bd6b3e41844e3257f4d603",
    "emailAddress": "codex-stage4-default@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | Default: `c9026d1f12bd6b3e41844e3257f4d603`. |
| `emailAddress` | string | yes | Default: `codex-stage4-default@example.com`. |
| `name` | string | no | Default: `Codex Default Subscriber`. |
| `resubscribe` | boolean | no | Default: `true`. |
| `consentToTrack` | string | no | Default: `Yes`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailAddress": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddress` | string | Email address of the subscriber that was added. |

## Native endpoint

Through the native CreateSend API, this operation is `POST /subscribers/:listId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subscriber.md) for the provider-specific parameters and requirements.

