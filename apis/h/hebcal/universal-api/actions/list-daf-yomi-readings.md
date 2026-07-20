# Hebcal: List Daf Yomi Readings

Retrieves Daf Yomi readings from Hebcal.

```
GET https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/list-daf-yomi-readings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hebcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/list-daf-yomi-readings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/list-daf-yomi-readings?${params}`, {
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
| `start` | string | no | Gregorian start date in YYYY-MM-DD format. |
| `end` | string | no | Gregorian end date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "items": [
        [
          {}
        ]
      ],
      "location": {
        "geo": "string"
      },
      "range": {
        "end": "2026-05-07T12:00:00.000Z",
        "start": "2026-05-07T12:00:00.000Z"
      },
      "title": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `items[]` | array<object> |  |
| `items[].category` | string |  |
| `items[].date` | date |  |
| `items[].hdate` | string |  |
| `items[].hebrew` | string |  |
| `items[].link` | string |  |
| `items[].title` | string |  |
| `location.geo` | string |  |
| `range.end` | date |  |
| `range.start` | date |  |
| `title` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Hebcal API, this operation is `GET /hebcal` (base URL `https://www.hebcal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-daf-yomi-readings.md) for the provider-specific parameters and requirements.

