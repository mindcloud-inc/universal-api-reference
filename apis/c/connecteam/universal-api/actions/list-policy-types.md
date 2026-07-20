# Connecteam: List Policy Types

Retrieve a list of policy types associated with the account

```
GET https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-policy-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-policy-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-policy-types?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "policies": [
        {
          "id": "string",
          "name": "Ava Chen",
          "unit": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `policies[].id` | string |  |
| `policies[].name` | string |  |
| `policies[].unit` | string |  |

## Native endpoint

Through the native Connecteam API, this operation is `GET /time-off/v1/policy-types` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-policy-types.md) for the provider-specific parameters and requirements.

