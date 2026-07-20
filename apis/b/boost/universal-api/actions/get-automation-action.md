# Boost: Get Automation Action

Retrieves an automation action from Boost by ID.

```
GET https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-automation-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-automation-action?connectionId=$CONNECTION_ID&actionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-automation-action?${params}`, {
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
| `actionId` | number | yes | Boost.space automation action ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Creation timestamp. |
| `id` | number | Automation action ID. |
| `name` | string | Action name. |
| `type` | string | Action type. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Boost API, this operation is `GET /automatization/action/{actionId}` (base URL `https://{{credentials.systemKey}}.boost.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-automation-action.md) for the provider-specific parameters and requirements.

