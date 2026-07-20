# Mocean API: Download Recording



```
GET https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/download-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/download-recording?connectionId=$CONNECTION_ID&callUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "callUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/download-recording?${params}`, {
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
| `callUuid` | string | yes | The call UUID for the recording. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callUuid": "string",
      "errMsg": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callUuid` | string |  |
| `errMsg` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Mocean API API, this operation is `GET /rest/2/voice/rec` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-recording.md) for the provider-specific parameters and requirements.

