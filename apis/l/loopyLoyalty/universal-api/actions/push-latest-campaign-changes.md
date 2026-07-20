# Loopy Loyalty: Push Latest Campaign Changes



```
PUT https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/push-latest-campaign-changes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/push-latest-campaign-changes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "5fcDywPejwj9QszwngBTKg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/push-latest-campaign-changes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "5fcDywPejwj9QszwngBTKg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Campaign ID to push updated changes to. Example: `5fcDywPejwj9QszwngBTKg`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the campaign changes were pushed successfully. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /campaign/:id/push` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/push-latest-campaign-changes.md) for the provider-specific parameters and requirements.

