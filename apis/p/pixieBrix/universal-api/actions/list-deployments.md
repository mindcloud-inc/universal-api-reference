# PixieBrix: List Deployments

Retrieves deployments from a PixieBrix organization.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-deployments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-deployments?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationPk=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationPk": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-deployments?${params}`, {
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
| `organizationPk` | string | yes | PixieBrix organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "bindings": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "organization": {},
      "package": {},
      "platforms": [
        {}
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `bindings` | array<object> |  |
| `created_at` | date |  |
| `id` | string |  |
| `name` | string |  |
| `organization` | object |  |
| `package` | object |  |
| `platforms` | array<object> |  |
| `updated_at` | date |  |

## Native endpoint

Through the native PixieBrix API, this operation is `GET /api/organizations/:organization_pk/deployments/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deployments.md) for the provider-specific parameters and requirements.

