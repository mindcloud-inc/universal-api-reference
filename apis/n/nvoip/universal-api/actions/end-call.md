# Nvoip: End Call



```
DELETE https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/end-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nvoip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/end-call?connectionId=$CONNECTION_ID&callId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "callId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/end-call?${params}`, {
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
| `callId` | string | yes | Unique Nvoip call identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "linkAudio": "https://example.com",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `linkAudio` | string | Recording link returned by Nvoip. |
| `state` | string | Provider result state for ending the call. |

## Native endpoint

Through the native Nvoip API, this operation is `GET /endcall` (base URL `https://api.nvoip.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/end-call.md) for the provider-specific parameters and requirements.

