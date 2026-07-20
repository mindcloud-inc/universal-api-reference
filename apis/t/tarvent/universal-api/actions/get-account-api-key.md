# Tarvent: Get Account API Key

Retrieves an account API key from Tarvent by ID.

```
GET https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/get-account-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tarvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/get-account-api-key?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/get-account-api-key?${params}`, {
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
| `variables.id` | string | yes | The Tarvent account API key ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audiences": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "permissionKeys": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audiences` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `permissionKeys` | array<string> |  |

## Native endpoint

Through the native Tarvent API, this operation is `POST /graphql` (base URL `https://api.tarvent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-api-key.md) for the provider-specific parameters and requirements.

