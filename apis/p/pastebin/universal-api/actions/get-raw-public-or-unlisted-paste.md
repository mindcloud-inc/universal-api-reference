# Pastebin: Get Raw Public Or Unlisted Paste

Retrieves raw content for a public or unlisted Pastebin paste.

```
GET https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/get-raw-public-or-unlisted-paste
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pastebin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/get-raw-public-or-unlisted-paste?connectionId=$CONNECTION_ID&pasteKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pasteKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/get-raw-public-or-unlisted-paste?${params}`, {
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
| `pasteKey` | string | yes | The Pastebin key for the public or unlisted paste. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw text content of the public or unlisted Pastebin paste. |

## Native endpoint

Through the native Pastebin API, this operation is `GET https://pastebin.com/raw/:pasteKey` (base URL `https://pastebin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-raw-public-or-unlisted-paste.md) for the provider-specific parameters and requirements.

