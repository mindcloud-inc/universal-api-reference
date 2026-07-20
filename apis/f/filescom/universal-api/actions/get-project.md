# Files.com: Get Project

Finds a project in Files.com by ID.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-project?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-project?${params}`, {
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
| `id` | number | yes | Numeric project ID. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "global_access": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `global_access` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /projects/:id` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

