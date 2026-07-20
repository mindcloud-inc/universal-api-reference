# Diffy: Get Project

Retrieves a single project from Diffy.

```
GET https://connect.mindcloud.co/v1/universal/diffy/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffy/latest/actions/get-project?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffy/latest/actions/get-project?${params}`, {
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
| `id` | number | yes | Project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "breakpoints": [
        1
      ],
      "development": "string",
      "name": "Ava Chen",
      "production": "string",
      "staging": "string",
      "urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `breakpoints` | array<number> | Configured breakpoints. |
| `development` | string | Development base URL. |
| `name` | string | Project name. |
| `production` | string | Production base URL. |
| `staging` | string | Staging base URL. |
| `urls` | array<string> | URLs included in the project. |

## Native endpoint

Through the native Diffy API, this operation is `GET /projects/:id` (base URL `https://app.diffy.website/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

