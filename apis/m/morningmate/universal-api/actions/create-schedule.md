# Morningmate: Create Schedule

Creates a schedule in a Morningmate project.

```
POST https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "registerId": "string",
  "title": "string",
  "isAllDay": true,
  "startDateTime": "string",
  "endDateTime": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "registerId": "string",
    "title": "string",
    "isAllDay": true,
    "startDateTime": "string",
    "endDateTime": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes |  |
| `registerId` | string | yes |  |
| `title` | string | yes |  |
| `isAllDay` | boolean | yes |  |
| `startDateTime` | string | yes |  |
| `endDateTime` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "postId": "string",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `postId` | string | Created schedule post identifier. |
| `projectId` | string | Morningmate project identifier. |

## Native endpoint

Through the native Morningmate API, this operation is `POST /v1/posts/projects/[:projectId]/schedules` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schedule.md) for the provider-specific parameters and requirements.

