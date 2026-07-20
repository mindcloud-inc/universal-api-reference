# Maildroppa: Count Subscribers

Counts Maildroppa subscribers by status.

```
GET https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/count-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/count-subscribers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/count-subscribers?${params}`, {
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
| `status` | string | no | Optional subscriber status to count. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formattedValue": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formattedValue` | string | Human-readable subscriber count. |
| `value` | number | Numeric subscriber count. |

## Native endpoint

Through the native Maildroppa API, this operation is `GET /subscribers/count` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-subscribers.md) for the provider-specific parameters and requirements.

