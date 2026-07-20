# xMatters: Delete a shift

Deletes a shift from your xMatters instance.

```
DELETE https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-shift?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-shift?${params}`, {
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
| `groupId` | string | no |  |
| `shiftId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "group": {
        "created": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "end": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "name": "Ava Chen",
        "recipientType": "string",
        "recurrence": {
          "end": {
            "endBy": "string"
          },
          "frequency": "string",
          "links": {
            "self": "https://example.com"
          },
          "onDays": [
            [
              "string"
            ]
          ],
          "repeatEvery": 1
        },
        "start": "2026-05-07T12:00:00.000Z",
        "targetName": "Ava Chen",
        "timezone": "string"
      },
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group.created` | date |  |
| `group.description` | string |  |
| `group.end` | date |  |
| `group.id` | string |  |
| `group.links.self` | string |  |
| `group.name` | string |  |
| `group.recipientType` | string |  |
| `group.recurrence.end.endBy` | string |  |
| `group.recurrence.frequency` | string |  |
| `group.recurrence.links.self` | string |  |
| `group.recurrence.onDays[]` | array<string> |  |
| `group.recurrence.repeatEvery` | number |  |
| `group.start` | date |  |
| `group.targetName` | string |  |
| `group.timezone` | string |  |
| `id` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `DELETE groups/{groupId}/shifts/{shiftId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-shift.md) for the provider-specific parameters and requirements.

