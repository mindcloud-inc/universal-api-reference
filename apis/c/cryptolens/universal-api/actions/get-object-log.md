# Cryptolens: Get Object Log

Retrieves object logs from Cryptolens.

```
GET https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-object-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-object-log?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-object-log?${params}`, {
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
| `limit` | number | no | Maximum number of object log entries to return. |
| `startingAfter` | number | no | Cursor for object log entries after the given id. |
| `v` | string | no | Method version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {}
      ],
      "message": "string",
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> | List of object log entries returned by Get Object Log. |
| `message` | string | Message returned by Get Object Log. |
| `result` | number | Result code returned by Get Object Log. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/ai/GetObjectLog` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-object-log.md) for the provider-specific parameters and requirements.

