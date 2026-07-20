# RD Station Marketing: List Popups



```
GET https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-popups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-popups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-popups?${params}`, {
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
      "conversionIdentifier": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "status": "string",
      "title": "string",
      "trigger": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversionIdentifier` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `status` | string |  |
| `title` | string |  |
| `trigger` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `GET /platform/popups` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-popups.md) for the provider-specific parameters and requirements.

