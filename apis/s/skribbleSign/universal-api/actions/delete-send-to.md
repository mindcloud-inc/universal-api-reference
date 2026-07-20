# Skribble Sign: Delete Send-To

Deletes an existing Send-To request from Skribble Sign.

```
DELETE https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/delete-send-to
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/delete-send-to?connectionId=$CONNECTION_ID&sendToId=string&accessCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sendToId": "string",
  "accessCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/delete-send-to?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the Send-To object was deleted. |

## Native endpoint

Through the native Skribble Sign API, this operation is `DELETE /v2/sendto/:sendToId` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-send-to.md) for the provider-specific parameters and requirements.

