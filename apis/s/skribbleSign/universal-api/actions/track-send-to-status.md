# Skribble Sign: Track Send-To Status

Retrieves Send-To delivery status from Skribble Sign.

```
GET https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/track-send-to-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/track-send-to-status?connectionId=$CONNECTION_ID&sendToId=string&accessCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sendToId": "string",
  "accessCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/track-send-to-status?${params}`, {
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
| `sendToId` | string | yes | The Send-To object ID. |
| `accessCode` | string | yes | The Send-To access code. This will be sent as the X-Accesscode header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creator": {},
      "signers": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creator` | object | Creator details. |
| `signers` | array<object> | Signer details. |
| `status` | string | Send-To status. |

## Native endpoint

Through the native Skribble Sign API, this operation is `GET /v2/sendto/:sendToId/track` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-send-to-status.md) for the provider-specific parameters and requirements.

