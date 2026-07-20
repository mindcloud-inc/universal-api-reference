# Confluent: List Service Accounts

Retrieves service accounts from Confluent Cloud.

```
GET https://connect.mindcloud.co/v1/universal/confluent/latest/actions/list-service-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluent `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/list-service-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluent/latest/actions/list-service-accounts?${params}`, {
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
| `displayName` | string | no | Filter the results by exact match for display_name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "data": [
        {
          "description": "string",
          "displayName": "Ava Chen",
          "id": "string"
        }
      ],
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
| `data` | array<object> |  |
| `data[].description` | string |  |
| `data[].displayName` | string |  |
| `data[].id` | string |  |
| `kind` | string |  |
| `metadata` | object |  |

## Native endpoint

Through the native Confluent API, this operation is `GET /iam/v2/service-accounts` (base URL `https://api.confluent.cloud`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-service-accounts.md) for the provider-specific parameters and requirements.

