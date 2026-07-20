# wttr.in: Get Moon Phase

Retrieves the moon phase for a date from wttr.in.

```
GET https://connect.mindcloud.co/v1/universal/wttrin/latest/actions/get-moon-phase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a wttr.in `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wttrin/latest/actions/get-moon-phase?connectionId=$CONNECTION_ID&moonDate=Moon%402026-04-30" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moonDate": "Moon@2026-04-30"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wttrin/latest/actions/get-moon-phase?${params}`, {
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
| `moonDate` | string | yes | Moon phase path segment in wttr.in syntax, such as Moon@2026-04-30. Example: `Moon@2026-04-30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | UTF-8 byte values for the moon phase output. |
| `type` | string | Runtime buffer marker for the raw moon phase text response. |

## Native endpoint

Through the native wttr.in API, this operation is `GET /[:moonDate]` (base URL `https://wttr.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-moon-phase.md) for the provider-specific parameters and requirements.

