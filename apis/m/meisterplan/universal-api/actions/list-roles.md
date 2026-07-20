# Meisterplan: List Roles

Retrieves a list of roles from Meisterplan.

```
GET https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-roles?${params}`, {
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
      "costPerHour": 1,
      "costType": "string",
      "externalId": "string",
      "id": "string",
      "name": "Ava Chen",
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
| `costPerHour` | number | Cost per hour |
| `costType` | string | Cost type |
| `externalId` | string | External ID |
| `id` | string | Role ID |
| `name` | string | Role name |
| `resourceManager.id` | string | Resource manager ID |
| `resourceManager.resourceKey` | string | Resource manager key |

## Native endpoint

Through the native Meisterplan API, this operation is `GET /roles` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-roles.md) for the provider-specific parameters and requirements.

