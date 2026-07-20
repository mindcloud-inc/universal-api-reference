# Reply: Lookup Prospect Id



```
GET https://connect.mindcloud.co/v1/universal/reply/latest/actions/lookup-prospect-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reply/latest/actions/lookup-prospect-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reply/latest/actions/lookup-prospect-id?${params}`, {
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
| `email` | string | no | Contact email address for prospect lookup. |
| `linkedin` | string | no | LinkedIn profile URL for prospect lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ids": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ids` | array<number> | Matching Reply prospect IDs. |

## Native endpoint

Through the native Reply API, this operation is `POST /v1/people/lookup` (base URL `https://api.reply.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-prospect-id.md) for the provider-specific parameters and requirements.

