# RotaCloud: List Day Notes V2



```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-day-notes-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-day-notes-v2?connectionId=$CONNECTION_ID&end=string&location=1&start=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "end": "string",
  "location": "1",
  "start": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-day-notes-v2?${params}`, {
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
| `end` | string | yes |  |
| `location` | number | yes |  |
| `start` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedAt": "string",
      "addedBy": 1,
      "endDate": "string",
      "id": 1,
      "locations": [
        1
      ],
      "message": "string",
      "startDate": "string",
      "title": "string",
      "updatedAt": "string",
      "updatedBy": 1,
      "visibleToEmployees": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedAt` | string |  |
| `addedBy` | number |  |
| `endDate` | string |  |
| `id` | number |  |
| `locations` | array<number> |  |
| `message` | string |  |
| `startDate` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `updatedBy` | number |  |
| `visibleToEmployees` | boolean |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v2/dayNotes` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-day-notes-v2.md) for the provider-specific parameters and requirements.

