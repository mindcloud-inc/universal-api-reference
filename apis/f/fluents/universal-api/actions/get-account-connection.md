# Fluents: Get Account Connection

Retrieves an account connection from Fluents.

```
GET https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-account-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-account-connection?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-account-connection?${params}`, {
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
| `id` | string | yes | Fluents account connection ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_supports_any_caller_id": true,
      "config": {},
      "credentials": {},
      "description": "string",
      "id": "string",
      "label": "string",
      "steering_pool": [
        "string"
      ],
      "type": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_supports_any_caller_id` | boolean |  |
| `config` | object |  |
| `credentials` | object |  |
| `description` | string |  |
| `id` | string |  |
| `label` | string |  |
| `steering_pool` | array<string> |  |
| `type` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Fluents API, this operation is `GET /account_connections` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-connection.md) for the provider-specific parameters and requirements.

