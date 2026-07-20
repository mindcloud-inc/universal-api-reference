# RD Station Marketing: List Emails



```
GET https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-emails?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "isPredictiveSending": true,
          "leadsCount": 1,
          "name": "Ava Chen",
          "sendAt": "2026-05-07T12:00:00.000Z",
          "sendingIsImminent": true,
          "status": "string",
          "type": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
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
| `items[].createdAt` | date |  |
| `items[].id` | number |  |
| `items[].isPredictiveSending` | boolean |  |
| `items[].leadsCount` | number |  |
| `items[].name` | string |  |
| `items[].sendAt` | date |  |
| `items[].sendingIsImminent` | boolean |  |
| `items[].status` | string |  |
| `items[].type` | string |  |
| `items[].updatedAt` | date |  |
| `total` | number |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `GET /platform/emails` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-emails.md) for the provider-specific parameters and requirements.

