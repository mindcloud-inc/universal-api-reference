# Sendcrux: Get Email List

Retrieves an email list from Sendcrux by UID.

```
GET https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/get-email-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/get-email-list?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/get-email-list?${params}`, {
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
| `uid` | string | yes | The unique identifier of the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {},
      "list": {},
      "statistics": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object |  |
| `list` | object |  |
| `statistics` | object |  |

## Native endpoint

Through the native Sendcrux API, this operation is `GET /api/v1/lists/:uid` (base URL `https://sendcrux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-list.md) for the provider-specific parameters and requirements.

