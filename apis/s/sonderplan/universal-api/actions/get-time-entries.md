# Sonderplan: Get Time Entries



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-time-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-time-entries?${params}`, {
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
      "description": "string",
      "durationSec": 1,
      "end": 1,
      "endDateTimeIso": "string",
      "id": 1,
      "name": "Ava Chen",
      "ownerId": 1,
      "start": 1,
      "startDateTimeIso": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `durationSec` | number |  |
| `end` | number |  |
| `endDateTimeIso` | string |  |
| `id` | number |  |
| `name` | string |  |
| `ownerId` | number |  |
| `start` | number |  |
| `startDateTimeIso` | string |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /time-entry` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entries.md) for the provider-specific parameters and requirements.

