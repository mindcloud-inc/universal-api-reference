# Realcrux: Get Mail List



```
GET https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/get-mail-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Realcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/get-mail-list?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/get-mail-list?${params}`, {
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
| `uid` | string | yes | UID of the Sendcrux mail list to inspect. |

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
| `contact` | object | List contact profile data. |
| `list` | object | Requested Realcrux mail list, including its custom field definitions. |
| `statistics` | object | Aggregate statistics for the mail list. |

## Native endpoint

Through the native Realcrux API, this operation is `GET lists/:uid` (base URL `https://sendcrux.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mail-list.md) for the provider-specific parameters and requirements.

