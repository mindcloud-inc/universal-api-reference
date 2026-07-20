# Sessionize: List Session Groups

Retrieves grouped event sessions from Sessionize.

```
GET https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/list-session-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sessionize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/list-session-groups?connectionId=$CONNECTION_ID&endpointId=jl4ktls0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endpointId": "jl4ktls0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/list-session-groups?${params}`, {
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
| `endpointId` | string | yes | Sessionize event API endpoint ID from URLs like https://sessionize.com/api/v2/{endpointId}/view/Sessions. Default: `jl4ktls0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupId": 1,
      "groupName": "Ava Chen",
      "isDefault": true,
      "sessions": [
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
| `groupId` | number | Session group/category identifier. |
| `groupName` | string | Session group/category name. |
| `isDefault` | boolean | Whether this is the default group. |
| `sessions` | array<object> | Sessions in this group. |

## Native endpoint

Through the native Sessionize API, this operation is `GET /api/v2/:endpointId/view/Sessions` (base URL `https://sessionize.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-session-groups.md) for the provider-specific parameters and requirements.

