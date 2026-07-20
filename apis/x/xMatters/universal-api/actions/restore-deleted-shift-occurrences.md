# xMatters: Restore deleted shift occurrences

Restores deleted shift occurrences in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/restore-deleted-shift-occurrences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/restore-deleted-shift-occurrences" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/restore-deleted-shift-occurrences', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endDate` | string | no |  |
| `groupId` | string | no |  |
| `shiftId` | string | no |  |
| `startDate` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "endDate": "2026-05-07T12:00:00.000Z",
          "startDate": "2026-05-07T12:00:00.000Z"
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
| `data[].endDate` | date |  |
| `data[].startDate` | date |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `POST groups/{groupId}/shifts/{shiftId}/occurrences` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-deleted-shift-occurrences.md) for the provider-specific parameters and requirements.

