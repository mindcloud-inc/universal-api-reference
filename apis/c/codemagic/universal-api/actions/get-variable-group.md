# Codemagic: Get Variable Group

Retrieves a specific variable group from Codemagic.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-variable-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-variable-group?connectionId=$CONNECTION_ID&variableGroupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variableGroupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-variable-group?${params}`, {
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
| `variableGroupId` | string | yes | Codemagic variable group identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advanced_security": {},
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advanced_security` | object |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/variable-groups/:variable_group_id` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variable-group.md) for the provider-specific parameters and requirements.

