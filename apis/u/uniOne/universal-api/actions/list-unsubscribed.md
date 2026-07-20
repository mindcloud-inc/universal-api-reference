# UniOne: List Unsubscribed

Retrieves unsubscribed email addresses from UniOne.

```
GET https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/list-unsubscribed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/list-unsubscribed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/list-unsubscribed?${params}`, {
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
| `dateFrom` | string | no | Return unsubscribed emails from this UTC date onward. Example: `2026-04-02`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "unsubscribed": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `unsubscribed` | array<object> |  |

## Native endpoint

Through the native UniOne API, this operation is `POST unsubscribed/list.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unsubscribed.md) for the provider-specific parameters and requirements.

