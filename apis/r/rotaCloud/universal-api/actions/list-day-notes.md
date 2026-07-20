# RotaCloud: List Day Notes

Lists day notes in RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-day-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-day-notes?connectionId=$CONNECTION_ID&start=string&end=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "string",
  "end": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-day-notes?${params}`, {
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
| `start` | string | yes | Start date for the day-note window in YYYY-MM-DD format. |
| `end` | string | yes | End date for the day-note window in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end_date": "string",
      "id": 1,
      "locations": [
        1
      ],
      "message": "string",
      "start_date": "string",
      "title": "string",
      "visible_employees": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end_date` | string |  |
| `id` | number |  |
| `locations` | array<number> |  |
| `message` | string |  |
| `start_date` | string |  |
| `title` | string |  |
| `visible_employees` | boolean |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/day_notes` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-day-notes.md) for the provider-specific parameters and requirements.

