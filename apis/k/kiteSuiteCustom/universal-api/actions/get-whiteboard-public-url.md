# Kite Suite: Get Whiteboard Public URL



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-whiteboard-public-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-whiteboard-public-url?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-whiteboard-public-url?${params}`, {
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
| `id` | string | yes | ID of the whiteboard. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "projectKey": "string",
      "url": "https://example.com",
      "workspaceKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projectKey` | string | Key of the project. |
| `url` | string | URL of the whiteboard. |
| `workspaceKey` | string | Key of the workspace. |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/white-board/public/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-whiteboard-public-url.md) for the provider-specific parameters and requirements.

