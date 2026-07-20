# xMatters: Get temporary absences

Retrieves temporary absences from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-temporary-absences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-temporary-absences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-temporary-absences?${params}`, {
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
| `groups` | string | no |  |
| `member` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "absenceType": "string",
          "end": "2026-05-07T12:00:00.000Z",
          "group": {
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "status": "string",
            "targetName": "Ava Chen"
          },
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "member": {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "status": "string",
            "targetName": "Ava Chen"
          },
          "replacement": {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "status": "string",
            "targetName": "Ava Chen"
          },
          "start": "2026-05-07T12:00:00.000Z"
        }
      ],
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
| `data[].absenceType` | string |  |
| `data[].end` | date |  |
| `data[].group.id` | string |  |
| `data[].group.links.self` | string |  |
| `data[].group.recipientType` | string |  |
| `data[].group.status` | string |  |
| `data[].group.targetName` | string |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].member.firstName` | string |  |
| `data[].member.id` | string |  |
| `data[].member.lastName` | string |  |
| `data[].member.links.self` | string |  |
| `data[].member.recipientType` | string |  |
| `data[].member.status` | string |  |
| `data[].member.targetName` | string |  |
| `data[].replacement.firstName` | string |  |
| `data[].replacement.id` | string |  |
| `data[].replacement.lastName` | string |  |
| `data[].replacement.links.self` | string |  |
| `data[].replacement.recipientType` | string |  |
| `data[].replacement.status` | string |  |
| `data[].replacement.targetName` | string |  |
| `data[].start` | date |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET temporary-absences` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-temporary-absences.md) for the provider-specific parameters and requirements.

