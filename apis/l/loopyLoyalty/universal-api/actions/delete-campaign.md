# Loopy Loyalty: Delete Campaign



```
DELETE https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/delete-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/delete-campaign?connectionId=$CONNECTION_ID&id=5fcDywPejwj9QszwngBTKg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "5fcDywPejwj9QszwngBTKg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/delete-campaign?${params}`, {
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
| `id` | string | yes | Example: `5fcDywPejwj9QszwngBTKg`. |

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
| `success` | boolean | Whether the campaign was deleted successfully. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `DELETE /campaign/:id` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-campaign.md) for the provider-specific parameters and requirements.

