# xMatters: Get shift occurrences

Retrieves shift occurrences from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-shift-occurrences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-shift-occurrences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-shift-occurrences?${params}`, {
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
          "end": "2026-05-07T12:00:00.000Z",
          "group": {
            "groupType": "string",
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "notifyEndOfEscalation": {
            "notifyEnabled": true
          },
          "shift": {
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "name": "Ava Chen"
          },
          "start": "2026-05-07T12:00:00.000Z"
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
| `data[].end` | date |  |
| `data[].group.groupType` | string |  |
| `data[].group.id` | string |  |
| `data[].group.links.self` | string |  |
| `data[].group.recipientType` | string |  |
| `data[].group.targetName` | string |  |
| `data[].notifyEndOfEscalation.notifyEnabled` | boolean |  |
| `data[].shift.id` | string |  |
| `data[].shift.links.self` | string |  |
| `data[].shift.name` | string |  |
| `data[].start` | date |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET groups/{groupId}/occurrences` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-shift-occurrences.md) for the provider-specific parameters and requirements.

