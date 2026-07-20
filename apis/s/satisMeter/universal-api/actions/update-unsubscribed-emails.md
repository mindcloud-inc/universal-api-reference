# SatisMeter: Update Unsubscribed Emails



```
PUT https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/update-unsubscribed-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SatisMeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/update-unsubscribed-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails": "user@example.com",
  "projectId": "61fce0adea447e24ec27d606"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/update-unsubscribed-emails', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails": "user@example.com",
    "projectId": "61fce0adea447e24ec27d606"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails` | list<string> | yes | Complete unsubscribe list to persist for the project. Provide the full desired set of unsubscribed email addresses. Example: `user@example.com`. |
| `projectId` | string | yes | Project ID. Example: `61fce0adea447e24ec27d606`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SatisMeter API returns.

## Native endpoint

Through the native SatisMeter API, this operation is `PATCH /api/v2/project-unsubscribes/:projectId` (base URL `https://app.satismeter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-unsubscribed-emails.md) for the provider-specific parameters and requirements.

