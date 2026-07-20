# GMass: Add Unsubscribed Domain

Unsubscribes a domain from your GMass account.

```
POST https://connect.mindcloud.co/v1/universal/gMass/latest/actions/add-unsubscribed-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/add-unsubscribed-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "codex-stage3.invalid"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gMass/latest/actions/add-unsubscribed-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "codex-stage3.invalid"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | Domain to add to the account unsubscribe domain list. Example: `codex-stage3.invalid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "unsubscribeTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string | Domain on the account unsubscribe domain list. |
| `unsubscribeTime` | date | Time the domain was unsubscribed. |

## Native endpoint

Through the native GMass API, this operation is `POST /unsubscribes/domain/:domain` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-unsubscribed-domain.md) for the provider-specific parameters and requirements.

