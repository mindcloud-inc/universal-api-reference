# Cloze: Retrieve Email Opens

Retrieves email opens from Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/retrieve-email-opens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/retrieve-email-opens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/retrieve-email-opens?${params}`, {
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
| `from` | number | no | UTC milliseconds timestamp for first message to retrieve. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorcode": 1,
      "messages": [
        [
          {}
        ]
      ],
      "more": true,
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorcode` | number | Error code. 0 means success. |
| `messages[]` | array<object> | Messages that have recorded opens. |
| `messages[].date` | number | UTC milliseconds when the message was sent. |
| `messages[].message` | string | URL to the message in Cloze. |
| `messages[].opens[]` | array<object> | Open events grouped by opener. |
| `messages[].opens[].about` | object | Information about the opener. |
| `messages[].opens[].breakdown[]` | array<object> | Individual open events. |
| `messages[].opens[].breakdown[].cookie` | string | Cookie identifier for the opener when present. |
| `messages[].opens[].breakdown[].date` | number | UTC milliseconds when the open occurred. |
| `messages[].threadId` | string | Thread identifier for the message. |
| `more` | boolean | Whether additional batches are available. |
| `next` | string | URL for the next batch of opens. |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/messages/opens` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-email-opens.md) for the provider-specific parameters and requirements.

