# RingCentral: Get Call Recording

Returns call recordings by ID(s).

```
GET https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-call-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RingCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-call-recording?connectionId=$CONNECTION_ID&accountId=~&recordingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "~",
  "recordingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-call-recording?${params}`, {
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
| `accountId` | string | yes | Internal identifier of the RingCentral account. Default value is "~" to indicate that the account associated with current authorization session should be used. Example: `~`. |
| `recordingId` | string | yes | Internal identifier of a call recording (returned in Call Log) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "contentUri": "string",
      "duration": 1,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `contentUri` | string |  |
| `duration` | number |  |
| `id` | string |  |

## Native endpoint

Through the native RingCentral API, this operation is `GET restapi/v1.0/account/:accountId/recording/:recordingId` (base URL `https://platform.ringcentral.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-recording.md) for the provider-specific parameters and requirements.

