# Daytona: Replace Sandbox Labels

Replaces sandbox labels in Daytona.

```
PUT https://connect.mindcloud.co/v1/universal/daytona/latest/actions/replace-sandbox-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/replace-sandbox-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sandboxIdOrName": "Ava Chen",
  "labels": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/daytona/latest/actions/replace-sandbox-labels', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sandboxIdOrName": "Ava Chen",
    "labels": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sandboxIdOrName` | string | yes | ID or name of the sandbox. |
| `labels` | object | yes | Key-value pairs of labels. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "labels": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `labels` | object | Key-value pairs of labels. |

## Native endpoint

Through the native Daytona API, this operation is `PUT /sandbox/[:sandboxIdOrName]/labels` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-sandbox-labels.md) for the provider-specific parameters and requirements.

