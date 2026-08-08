# XOi: Get Groups



```
GET https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XOi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-groups?connectionId=$CONNECTION_ID&groupIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-groups?${params}`, {
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
| `groupIds[]` | array<string> | yes | XOi group ids input. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "members": [
        "string"
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `members` | array<string> |  |
| `name` | string |  |

## Native endpoint

Through the native XOi API, this operation is `POST https://gql-users-external.xoi.io/graphql` (base URL `https://gql-jobs-external.xoi.io/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-groups.md) for the provider-specific parameters and requirements.

