# Kite Suite: Get Workspace



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-workspace?${params}`, {
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
| `id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "tenant": "string",
      "totalMemoryCapacity": 1,
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the notification |
| `id` | string |  |
| `name` | string | name of workspace |
| `tenant` | string | tenant id |
| `totalMemoryCapacity` | number | total memory capacity (default is 2GB) |
| `type` | string | workspace type |
| `url` | string | url of workspace |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/workspace/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

