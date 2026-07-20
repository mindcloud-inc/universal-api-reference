# National Park Service: List Events

Retrieves events from National Park Service.

```
GET https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a National Park Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-events?${params}`, {
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
| `dateEnd` | string | no | End date in yyyy-mm-dd format. |
| `dateStart` | string | no | Start date in yyyy-mm-dd format. |
| `pageNumber` | string | no | Event results page number. NPS defaults to 1. |
| `pageSize` | string | no | Number of events per page. NPS defaults to 10. |
| `parkCode` | string | no | Comma-delimited NPS park codes. |
| `q` | string | no | Search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "errors": [
        {}
      ],
      "pagenumber": "string",
      "pagesize": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `errors` | array<object> |  |
| `pagenumber` | string |  |
| `pagesize` | string |  |
| `total` | string |  |

## Native endpoint

Through the native National Park Service API, this operation is `GET /events` (base URL `https://developer.nps.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

