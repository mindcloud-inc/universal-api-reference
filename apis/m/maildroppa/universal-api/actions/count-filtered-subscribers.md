# Maildroppa: Count Filtered Subscribers

Counts Maildroppa subscribers by segment expression.

```
GET https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/count-filtered-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/count-filtered-subscribers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/count-filtered-subscribers?${params}`, {
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
| `filterGroups[]` | array | no | Filter groups that compose this expression. |
| `operator` | string | no | Logical operator that applies between filter groups. |
| `status` | string | no | Subscriber status filter. |

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
| `formattedValue` | string | A formatted string representation of the numeric value. This might include locale-specific formatting like commas or currency symbols. |
| `value` | number | The numeric value. |

## Native endpoint

Through the native Maildroppa API, this operation is `POST /subscribers/filtered-count` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-filtered-subscribers.md) for the provider-specific parameters and requirements.

