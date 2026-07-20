# Moderation API: Get Embedding Status

Retrieves wordlist embedding status from Moderation API.

```
GET https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-embedding-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-embedding-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-embedding-status?${params}`, {
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
| `id` | string | yes | ID of the wordlist to check embedding status for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "progress": 1,
      "remainingWords": 1,
      "totalWords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `progress` | number | Percentage of words that have been embedded (0-100) |
| `remainingWords` | number | Number of words still waiting to be embedded |
| `totalWords` | number | Total number of words in the wordlist |

## Native endpoint

Through the native Moderation API API, this operation is `GET /wordlist/:id/embedding-status` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-embedding-status.md) for the provider-specific parameters and requirements.

