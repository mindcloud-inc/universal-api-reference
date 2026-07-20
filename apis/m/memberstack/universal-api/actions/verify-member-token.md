# Memberstack: Verify Member Token



```
GET https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/verify-member-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memberstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/verify-member-token?connectionId=$CONNECTION_ID&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/verify-member-token?${params}`, {
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
| `token` | string | yes | Member JWT token to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auth": {},
      "customFields": {},
      "id": "string",
      "metaData": {},
      "permissions": [
        "string"
      ],
      "valid": true,
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth` | object |  |
| `customFields` | object |  |
| `id` | string |  |
| `metaData` | object |  |
| `permissions` | array<string> |  |
| `valid` | boolean |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Memberstack API, this operation is `POST /members/verify-token` (base URL `https://admin.memberstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-member-token.md) for the provider-specific parameters and requirements.

