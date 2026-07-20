# condoo: Retrieve Goal Conversion

Retrieves a goal conversion from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-goal-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-goal-conversion?connectionId=$CONNECTION_ID&conversionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-goal-conversion?${params}`, {
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
| `conversionId` | number | yes | Required goal conversion ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datetime": "2026-05-07T12:00:00.000Z",
      "event_id": 1,
      "id": 1,
      "session_id": 1,
      "user_id": 1,
      "visitor_id": 1,
      "website_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datetime` | date |  |
| `event_id` | number |  |
| `id` | number |  |
| `session_id` | number |  |
| `user_id` | number |  |
| `visitor_id` | number |  |
| `website_id` | number |  |

## Native endpoint

Through the native condoo API, this operation is `GET /goals-conversions/{conversion_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-goal-conversion.md) for the provider-specific parameters and requirements.

