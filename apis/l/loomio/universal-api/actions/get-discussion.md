# Loomio: Get Discussion

Retrieves a discussion from Loomio.

```
GET https://connect.mindcloud.co/v1/universal/loomio/latest/actions/get-discussion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loomio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loomio/latest/actions/get-discussion?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loomio/latest/actions/get-discussion?${params}`, {
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
| `id` | string | no | The Loomio discussion ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `meta` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Loomio API, this operation is `GET /discussions/:id` (base URL `https://www.loomio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-discussion.md) for the provider-specific parameters and requirements.

