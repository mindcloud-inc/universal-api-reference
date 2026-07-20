# Confluent: Read IP Filter

Retrieves an IP filter from Confluent Cloud.

```
GET https://connect.mindcloud.co/v1/universal/confluent/latest/actions/read-ip-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/read-ip-filter?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluent/latest/actions/read-ip-filter?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |

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

Through the native Confluent API, this operation is `GET /iam/v2/ip-filters/:id` (base URL `https://api.confluent.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-ip-filter.md) for the provider-specific parameters and requirements.

