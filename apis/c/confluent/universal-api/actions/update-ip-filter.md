# Confluent: Update IP Filter

Updates an existing IP filter in Confluent Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/confluent/latest/actions/update-ip-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/update-ip-filter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/confluent/latest/actions/update-ip-filter', {
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
| `id` | string | yes |  |
| `filterName` | string | no |  |
| `resourceGroup` | string | no |  |
| `resourceScope` | string | no |  |
| `operationGroups[]` | array<string> | no |  |
| `ipGroups[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "filterName": "Ava Chen",
      "id": "string",
      "ipGroups": [
        {}
      ],
      "kind": "string",
      "metadata": {},
      "operationGroups": [
        {}
      ],
      "resourceGroup": "string",
      "resourceScope": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `filterName` | string |  |
| `id` | string |  |
| `ipGroups` | array<object> |  |
| `kind` | string |  |
| `metadata` | object |  |
| `operationGroups` | array<object> |  |
| `resourceGroup` | string |  |
| `resourceScope` | string |  |

## Native endpoint

Through the native Confluent API, this operation is `PATCH /iam/v2/ip-filters/:id` (base URL `https://api.confluent.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ip-filter.md) for the provider-specific parameters and requirements.

