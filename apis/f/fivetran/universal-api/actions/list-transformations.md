# Fivetran: List Transformations

Retrieves transformations from your Fivetran account.

```
GET https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/list-transformations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/list-transformations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/list-transformations?${params}`, {
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
| `groupId` | string | no | Filter transformations by group ID. |
| `projectId` | string | no | Filter transformations by dbt Core project ID. |
| `type` | string | no | Filter transformations by type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupId": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Fivetran API, this operation is `GET /transformations` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transformations.md) for the provider-specific parameters and requirements.

