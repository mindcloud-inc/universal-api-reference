# Svix: List Endpoints

Retrieves endpoints from Svix.

```
GET https://connect.mindcloud.co/v1/universal/svix/latest/actions/list-endpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/list-endpoints?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/list-endpoints?${params}`, {
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
| `appId` | string | yes | The application's ID or UID. |
| `iterator` | string | no | The iterator returned from a prior invocation. |
| `limit` | number | no | Limit the number of returned items. |
| `order` | string | no | The sorting order of the returned items. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "done": true,
      "iterator": "string",
      "prevIterator": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `done` | boolean |  |
| `iterator` | string |  |
| `prevIterator` | string |  |

## Native endpoint

Through the native Svix API, this operation is `GET /api/v1/app/{app_id}/endpoint` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-endpoints.md) for the provider-specific parameters and requirements.

