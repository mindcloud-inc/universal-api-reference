# SmartrMail: Get Subscriber List

Retrieves a subscriber list from SmartrMail.

```
GET https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/get-subscriber-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartrMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/get-subscriber-list?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/get-subscriber-list?${params}`, {
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
| `listId` | string | yes | The ID of the requested list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "subscribers_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `subscribers_count` | number |  |

## Native endpoint

Through the native SmartrMail API, this operation is `GET /lists/:list_id` (base URL `https://go.smartrmail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber-list.md) for the provider-specific parameters and requirements.

