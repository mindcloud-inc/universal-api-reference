# InstantCard: Submit Print Job

Updates an existing print job in InstantCard by submitting it.

```
PUT https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/submit-print-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/submit-print-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "20003827",
  "id": "1614262"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/submit-print-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "20003827",
    "id": "1614262"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes | Organization ID from your InstantCard account. Example: `20003827`. |
| `id` | number | yes | ID of the print job to submit. Example: `1614262`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native InstantCard API returns.

## Native endpoint

Through the native InstantCard API, this operation is `POST /api/v2/organizations/:organizationId/print_jobs/:id/print` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-print-job.md) for the provider-specific parameters and requirements.

