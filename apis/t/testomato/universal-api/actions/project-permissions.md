# Testomato: Project permissions

Retrieves project permissions from Testomato.

```
GET https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-permissions?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-permissions?${params}`, {
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
      "apiKey": true,
      "edit": true,
      "editTests": true,
      "manageUsers": true,
      "read": true,
      "run": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | boolean |  |
| `edit` | boolean |  |
| `editTests` | boolean |  |
| `manageUsers` | boolean |  |
| `read` | boolean |  |
| `run` | boolean |  |

## Native endpoint

Through the native Testomato API, this operation is `GET /project/:id/permissions` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/project-permissions.md) for the provider-specific parameters and requirements.

