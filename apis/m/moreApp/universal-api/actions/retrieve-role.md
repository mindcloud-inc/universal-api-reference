# MoreApp: Retrieve Role

Retrieves a role from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-role?connectionId=$CONNECTION_ID&customerId=1&roleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "roleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-role?${params}`, {
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
| `customerId` | number | yes |  |
| `roleId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultOn": "string",
      "id": "string",
      "name": "Ava Chen",
      "permissions": [
        "string"
      ],
      "readOnly": true,
      "translatableKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultOn` | string |  |
| `id` | string |  |
| `name` | string |  |
| `permissions` | array<string> |  |
| `readOnly` | boolean |  |
| `translatableKey` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v2/customers/{{customerId}}/roles/{{roleId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-role.md) for the provider-specific parameters and requirements.

