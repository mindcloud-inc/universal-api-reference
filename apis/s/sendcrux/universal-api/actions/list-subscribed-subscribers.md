# Sendcrux: List Subscribed Subscribers

Retrieves subscribed subscribers from a Sendcrux email list.

```
GET https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/list-subscribed-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/list-subscribed-subscribers?connectionId=$CONNECTION_ID&list_uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list_uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/list-subscribed-subscribers?${params}`, {
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
| `list_uid` | string | yes | The UID of the list whose subscribed subscribers you want to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "COMPANY": "string",
      "COUNTRY": "string",
      "email": "ava@example.com",
      "FIRST_NAME": "Ava",
      "LAST_NAME": "Chen",
      "mxrecords": "string",
      "mxrecords_rawvalue": "string",
      "PHONE_NUMBER": "string",
      "status": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `COMPANY` | string |  |
| `COUNTRY` | string |  |
| `email` | string |  |
| `FIRST_NAME` | string |  |
| `LAST_NAME` | string |  |
| `mxrecords` | string |  |
| `mxrecords_rawvalue` | string |  |
| `PHONE_NUMBER` | string |  |
| `status` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Sendcrux API, this operation is `GET /api/v1/subscribers` (base URL `https://sendcrux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribed-subscribers.md) for the provider-specific parameters and requirements.

