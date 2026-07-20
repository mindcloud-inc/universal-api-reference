# CastingWords: Send Transcript Complete Webhook Test

Sends a transcript complete webhook test from CastingWords.

```
POST https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/send-transcript-complete-webhook-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CastingWords `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/send-transcript-complete-webhook-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/send-transcript-complete-webhook-test', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "success": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | number | Provider success flag. |

## Native endpoint

Through the native CastingWords API, this operation is `POST webhook/test/TRANSCRIPT_COMPLETE` (base URL `https://castingwords.com/store/API4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transcript-complete-webhook-test.md) for the provider-specific parameters and requirements.

