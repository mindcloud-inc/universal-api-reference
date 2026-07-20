# Assembly.com: Update Company

Updates an existing company in Assembly.com.

```
PUT https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the company to be updated. |
| `name` | string | no | The company’s new name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields` | object | no | Optional custom field updates keyed by Assembly custom field keys. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Assembly.com API returns.

## Native endpoint

Through the native Assembly.com API, this operation is `PATCH /companies/:id` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

