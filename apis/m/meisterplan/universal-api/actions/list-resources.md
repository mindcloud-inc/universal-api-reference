# Meisterplan: List Resources

Retrieves a list of resources from Meisterplan.

```
GET https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-resources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-resources?${params}`, {
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
| `filter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendar": {
        "id": "string",
        "path": "string"
      },
      "costPerHour": 1,
      "emailAddress": "ava@example.com",
      "externalId": "string",
      "externalResource": true,
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "primaryRole": {
        "id": "string",
        "name": "Ava Chen"
      },
      "resourceKey": "string",
      "resourceManager": {
        "id": "string",
        "resourceKey": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendar.id` | string | Calendar ID |
| `calendar.path` | string | Calendar path |
| `costPerHour` | number | Cost per hour |
| `emailAddress` | string | Email address |
| `externalId` | string | External ID |
| `externalResource` | boolean | External resource flag |
| `firstName` | string | First name |
| `id` | string | Resource ID |
| `lastName` | string | Last name |
| `primaryRole.id` | string | Primary role ID |
| `primaryRole.name` | string | Primary role name |
| `resourceKey` | string | Resource key |
| `resourceManager.id` | string | Resource manager ID |
| `resourceManager.resourceKey` | string | Resource manager key |

## Native endpoint

Through the native Meisterplan API, this operation is `GET /resources` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-resources.md) for the provider-specific parameters and requirements.

