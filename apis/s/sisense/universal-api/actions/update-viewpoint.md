# Sisense: Update Viewpoint

Updates an existing viewpoint in Sisense.

```
PUT https://connect.mindcloud.co/v1/universal/sisense/latest/actions/update-viewpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/update-viewpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sisense/latest/actions/update-viewpoint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | The updated viewpoint description. |
| `id` | string | no | The Viewpoint identifier. |
| `name` | string | no | The updated viewpoint name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `PUT /api/v1/infusion/viewpoints/:id` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-viewpoint.md) for the provider-specific parameters and requirements.

