# Quentn: List Contact Terms



```
GET https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-contact-terms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-contact-terms?connectionId=$CONNECTION_ID&contact_id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-contact-terms?${params}`, {
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
| `contact_id` | number | yes | The numeric Quentn contact id whose terms you want to list. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "terms": [
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
| `terms` | array<object> |  |

## Native endpoint

Through the native Quentn API, this operation is `GET /contact/:contact_id/terms` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-terms.md) for the provider-specific parameters and requirements.

