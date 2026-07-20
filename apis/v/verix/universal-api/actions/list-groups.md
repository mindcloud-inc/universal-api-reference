# Verix: List Groups

Retrieves credential groups from your Verix account.

```
GET https://connect.mindcloud.co/v1/universal/verix/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verix/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verix/latest/actions/list-groups?${params}`, {
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
| `pageNumber` | string | no | 1-based page number to retrieve. |
| `pageSize` | string | no | Number of groups to return per page. Verix defaults to 10. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": 1,
      "description": "string",
      "id": 1,
      "issuedRecipient": 1,
      "name": "Ava Chen",
      "templateImageRelUrl": "https://example.com",
      "totalRecipient": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | number | Unix timestamp when the group was created. |
| `description` | string | Group description. |
| `id` | number | Unique identifier for the group. |
| `issuedRecipient` | number | Recipients already issued credentials. |
| `name` | string | Group name. |
| `templateImageRelUrl` | string | Relative URL of the template image. |
| `totalRecipient` | number | Total recipients in the group. |

## Native endpoint

Through the native Verix API, this operation is `GET /v1/credentials/groups` (base URL `https://api.verix.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

