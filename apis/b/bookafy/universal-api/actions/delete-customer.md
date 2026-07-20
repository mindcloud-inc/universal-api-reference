# Bookafy: Delete Customer

Deletes a customer from Bookafy.

```
DELETE https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/delete-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookafy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/delete-customer?connectionId=$CONNECTION_ID&id=2980611" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "2980611"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/delete-customer?${params}`, {
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
| `id` | number | yes | Customer ID from Bookafy. Example: `2980611`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response.message` | string | Bookafy status message for the delete request. |

## Native endpoint

Through the native Bookafy API, this operation is `DELETE /customers/:id` (base URL `https://app.bookafy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer.md) for the provider-specific parameters and requirements.

