# Flexmail: Delete Interest Subscription

Deletes an interest subscription from a contact in Flexmail.

```
DELETE https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/delete-interest-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexmail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/delete-interest-subscription?connectionId=$CONNECTION_ID&id=1&interestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "interestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/delete-interest-subscription?${params}`, {
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
| `id` | number | yes |  |
| `interestId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Placeholder schema for the documented no-content success response. |

## Native endpoint

Through the native Flexmail API, this operation is `DELETE /contacts/{id}/interest-subscriptions/{interest_id}` (base URL `https://api.flexmail.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-interest-subscription.md) for the provider-specific parameters and requirements.

