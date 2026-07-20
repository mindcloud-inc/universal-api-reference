# Meisterplan: Get Role

Retrieves a role from Meisterplan.

```
GET https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-role?connectionId=$CONNECTION_ID&roleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-role?${params}`, {
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
| `roleId` | string | yes |  |

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
      "name": "Ava Chen"
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

## Native endpoint

Through the native Meisterplan API, this operation is `GET /roles/:roleId` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-role.md) for the provider-specific parameters and requirements.

