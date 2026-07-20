# Confluent: Create IP Group

Creates a new IP group in Confluent Cloud.

```
POST https://connect.mindcloud.co/v1/universal/confluent/latest/actions/create-ip-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/create-ip-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupName": "Ava Chen",
  "cidrBlocks[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/confluent/latest/actions/create-ip-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupName": "Ava Chen",
    "cidrBlocks[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupName` | string | yes |  |
| `cidrBlocks[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "cidrBlocks": [
        "string"
      ],
      "groupName": "Ava Chen",
      "id": "string",
      "kind": "string",
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `cidrBlocks` | array<string> |  |
| `groupName` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `metadata` | object |  |

## Native endpoint

Through the native Confluent API, this operation is `POST /iam/v2/ip-groups` (base URL `https://api.confluent.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ip-group.md) for the provider-specific parameters and requirements.

