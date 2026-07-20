# Pixela: List Graphs

Retrieves all graph definitions in Pixela.

```
GET https://connect.mindcloud.co/v1/universal/pixela/latest/actions/list-graphs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixela `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/list-graphs?connectionId=$CONNECTION_ID&username=a-know" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "a-know"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixela/latest/actions/list-graphs?${params}`, {
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
| `username` | string | yes | Pixela username in the request path. Use the Pixela username, not an email address. Example: `a-know`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "description": "string",
      "id": "string",
      "isSecret": true,
      "name": "Ava Chen",
      "publishOptionalData": true,
      "purgeCacheURLs": [
        "https://example.com"
      ],
      "selfSufficient": "string",
      "startOnMonday": true,
      "timezone": "string",
      "type": "string",
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isSecret` | boolean |  |
| `name` | string |  |
| `publishOptionalData` | boolean |  |
| `purgeCacheURLs` | array<string> |  |
| `selfSufficient` | string |  |
| `startOnMonday` | boolean |  |
| `timezone` | string |  |
| `type` | string |  |
| `unit` | string |  |

## Native endpoint

Through the native Pixela API, this operation is `GET /v1/users/:username/graphs` (base URL `https://pixe.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-graphs.md) for the provider-specific parameters and requirements.

