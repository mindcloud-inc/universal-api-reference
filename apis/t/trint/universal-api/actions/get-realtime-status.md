# Trint: Get Realtime Status

Retrieves realtime transcript status from Trint.

```
GET https://connect.mindcloud.co/v1/universal/trint/latest/actions/get-realtime-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trint/latest/actions/get-realtime-status?connectionId=$CONNECTION_ID&trintId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trintId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trint/latest/actions/get-realtime-status?${params}`, {
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
| `trintId` | string | yes | The Trint file identifier for the realtime transcript. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Current realtime transcript status. |

## Native endpoint

Through the native Trint API, this operation is `GET /transcripts/realtime/:trintId` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-realtime-status.md) for the provider-specific parameters and requirements.

