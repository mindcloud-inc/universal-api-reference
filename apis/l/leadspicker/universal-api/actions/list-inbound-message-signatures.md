# Leadspicker: List Inbound Message Signatures

Retrieves inbound message signatures from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-inbound-message-signatures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-inbound-message-signatures?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-inbound-message-signatures?${params}`, {
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
      "channel": "string",
      "direction": "string",
      "last_ts": 1,
      "person_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `direction` | string |  |
| `last_ts` | number |  |
| `person_id` | number |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/inbound-messages/signatures` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inbound-message-signatures.md) for the provider-specific parameters and requirements.

