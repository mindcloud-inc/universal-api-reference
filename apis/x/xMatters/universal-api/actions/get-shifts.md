# xMatters: Get shifts

Retrieves shifts from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-shifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-shifts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-shifts?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "created": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "end": "2026-05-07T12:00:00.000Z",
          "group": {
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen",
          "notifyEndOfEscalation": {
            "notifyEnabled": "string"
          },
          "recurrence": {
            "end": {
              "endBy": "string"
            },
            "frequency": "string",
            "onDays": [
              [
                "string"
              ]
            ],
            "repeatEvery": 1
          },
          "repeatEscalation": {
            "repeatEnabled": "string"
          },
          "start": "2026-05-07T12:00:00.000Z",
          "timezone": "string"
        }
      ],
      "links": {
        "self": "https://example.com"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].created` | date |  |
| `data[].description` | string |  |
| `data[].end` | date |  |
| `data[].group.id` | string |  |
| `data[].group.links.self` | string |  |
| `data[].group.recipientType` | string |  |
| `data[].group.targetName` | string |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].name` | string |  |
| `data[].notifyEndOfEscalation.notifyEnabled` | string |  |
| `data[].recurrence.end.endBy` | string |  |
| `data[].recurrence.frequency` | string |  |
| `data[].recurrence.onDays[]` | array<string> |  |
| `data[].recurrence.repeatEvery` | number |  |
| `data[].repeatEscalation.repeatEnabled` | string |  |
| `data[].start` | date |  |
| `data[].timezone` | string |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET groups/{groupId}/shifts` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-shifts.md) for the provider-specific parameters and requirements.

