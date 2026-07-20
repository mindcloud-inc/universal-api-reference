# Ayrshare: Check Banned Hashtag

Checks whether a hashtag is banned in Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/check-banned-hashtag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/check-banned-hashtag?connectionId=$CONNECTION_ID&hashtag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hashtag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/check-banned-hashtag?${params}`, {
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
| `hashtag` | string | yes | Hashtag to check, including the leading # when available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "banned": true,
      "code": 1,
      "hashtag": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `banned` | boolean | Whether the hashtag is banned. |
| `code` | number | Ayrshare error code. |
| `hashtag` | string | Checked hashtag. |
| `message` | string | Check or error message. |
| `status` | string | Response status. |

## Native endpoint

Through the native Ayrshare API, this operation is `GET /hashtags/banned` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-banned-hashtag.md) for the provider-specific parameters and requirements.

