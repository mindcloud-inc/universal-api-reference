# Boost: Get Automation Trigger

Retrieves an automation trigger from Boost by ID.

```
GET https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-automation-trigger
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-automation-trigger?connectionId=$CONNECTION_ID&triggerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "triggerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-automation-trigger?${params}`, {
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
| `triggerId` | number | yes | Boost.space automation trigger ID. |

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
| `id` | number | Trigger ID. |
| `name` | string | Trigger name. |
| `type` | string | Trigger type. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Boost API, this operation is `GET /automatization/trigger/{triggerId}` (base URL `https://{{credentials.systemKey}}.boost.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-automation-trigger.md) for the provider-specific parameters and requirements.

