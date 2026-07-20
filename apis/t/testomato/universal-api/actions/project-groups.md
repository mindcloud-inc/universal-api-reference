# Testomato: Project groups

Retrieves project groups from Testomato.

```
GET https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-groups?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-groups?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "nextRun": 1,
      "options": {},
      "period": true,
      "periodInt": 1,
      "projectId": "string",
      "public": true,
      "rules": [
        {}
      ]
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
| `nextRun` | number |  |
| `options` | object |  |
| `period` | boolean |  |
| `periodInt` | number |  |
| `projectId` | string |  |
| `public` | boolean |  |
| `rules` | array<object> |  |

## Native endpoint

Through the native Testomato API, this operation is `GET /project/:id/areas` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/project-groups.md) for the provider-specific parameters and requirements.

