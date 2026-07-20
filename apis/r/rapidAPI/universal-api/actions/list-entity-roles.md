# RapidAPI: List Entity Roles

Retrieves roles for an entity in RapidAPI.

```
GET https://connect.mindcloud.co/v1/universal/rapidAPI/latest/actions/list-entity-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RapidAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rapidAPI/latest/actions/list-entity-roles?connectionId=$CONNECTION_ID&entityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rapidAPI/latest/actions/list-entity-roles?${params}`, {
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
| `entityId` | string | yes | RapidAPI entity ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orgId": "string",
      "role": {
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orgId` | string |  |
| `role.name` | string |  |

## Native endpoint

Through the native RapidAPI API, this operation is `GET /admin/entities/{entityId}/roles` (base URL `{{credentials.baseUrlRest}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-entity-roles.md) for the provider-specific parameters and requirements.

