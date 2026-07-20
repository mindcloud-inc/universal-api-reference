# Microsoft 365 Planner: Get Group



```
GET https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-group?connectionId=$CONNECTION_ID&groupId=9b1f3c7a-1234-4abc-9def-123456789abc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "9b1f3c7a-1234-4abc-9def-123456789abc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-group?${params}`, {
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
| `groupId` | string | yes | Microsoft 365 group ID to retrieve. Example: `9b1f3c7a-1234-4abc-9def-123456789abc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "displayName": "Ava Chen",
      "groupTypes": [
        "string"
      ],
      "id": "string",
      "mailNickname": "Ava Chen",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `displayName` | string |  |
| `groupTypes` | array<string> |  |
| `id` | string |  |
| `mailNickname` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Microsoft 365 Planner API, this operation is `GET /v1.0/groups/{{groupId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

