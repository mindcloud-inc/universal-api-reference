# Codemagic: List Variables For Group

Retrieves variables for a specific Codemagic variable group.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-variables-for-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-variables-for-group?connectionId=$CONNECTION_ID&limit=25&offset=0&variableGroupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "variableGroupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-variables-for-group?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `search` | string | no | Optional variable search string. |

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

Through the native Codemagic API, this operation is `GET /api/v3/variable-groups/:variable_group_id/variables` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-variables-for-group.md) for the provider-specific parameters and requirements.

