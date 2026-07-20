# Endear: List Teams



```
GET https://connect.mindcloud.co/v1/universal/endear/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Endear `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/endear/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/endear/latest/actions/list-teams?${params}`, {
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
| `variables.first` | number | no | First for the Endear GraphQL operation. |
| `variables.after` | string | no | After for the Endear GraphQL operation. |
| `variables.search` | string | no | Search for the Endear GraphQL operation. |
| `variables.accessibleToUserId` | string | no | Accessible To User Id for the Endear GraphQL operation. |
| `variables.teamMemberIds[]` | array<string> | no | Team Member Ids for the Endear GraphQL operation. |
| `variables.byStatus` | string | no | By Status for the Endear GraphQL operation. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.sortBy` | string | no | Sort By for the Endear GraphQL operation. |
| `variables.sortDir` | string | no | Sort Dir for the Endear GraphQL operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
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
| `cursor` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Endear API, this operation is `POST /graphql` (base URL `https://api.endearhq.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

