# UpGuard: Update Domain Labels

Updates labels for a domain in UpGuard.

```
PUT https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/update-domain-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/update-domain-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hostname": "Ava Chen",
  "labels": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/update-domain-labels', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hostname": "Ava Chen",
    "labels": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hostname` | string | yes | The hostname to update labels for |
| `labels` | string<string> | yes | The labels to assign to the domain. You can pass an empty array to remove all labels. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UpGuard API returns.

## Native endpoint

Through the native UpGuard API, this operation is `PUT /domain/labels` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-domain-labels.md) for the provider-specific parameters and requirements.

