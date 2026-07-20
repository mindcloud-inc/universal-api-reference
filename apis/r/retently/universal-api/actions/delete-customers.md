# Retently: Delete Customers

Deletes existing customer records from Retently.

```
DELETE https://connect.mindcloud.co/v1/universal/retently/latest/actions/delete-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/retently/latest/actions/delete-customers?connectionId=$CONNECTION_ID&subscribers%5B%5D=string&subscribers%5B%5D.email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscribers[]": "string",
  "subscribers[].email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/delete-customers?${params}`, {
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
| `subscribers[]` | array<string> | yes | An array of subscriber emails |
| `subscribers[].email` | string | yes | Email address |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `email` | string |  |

## Native endpoint

Through the native Retently API, this operation is `DELETE /api/v2/customers` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customers.md) for the provider-specific parameters and requirements.

