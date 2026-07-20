# Codemagic: Get Variable

Retrieves a specific variable from a Codemagic group.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-variable?connectionId=$CONNECTION_ID&variableGroupId=string&variableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variableGroupId": "string",
  "variableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-variable?${params}`, {
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
| `variableId` | string | yes | Codemagic environment variable identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "secure": true,
      "value": "string"
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
| `secure` | boolean |  |
| `value` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/variable-groups/:variable_group_id/variables/:variable_id` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variable.md) for the provider-specific parameters and requirements.

