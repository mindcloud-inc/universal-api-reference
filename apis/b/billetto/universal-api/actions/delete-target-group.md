# Billetto: Delete Target Group

Deletes a target group from Billetto.

```
DELETE https://connect.mindcloud.co/v1/universal/billetto/latest/actions/delete-target-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billetto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/billetto/latest/actions/delete-target-group?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billetto/latest/actions/delete-target-group?${params}`, {
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
| `id` | string | yes | Billetto target group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | string |  |
| `object` | string |  |

## Native endpoint

Through the native Billetto API, this operation is `DELETE organiser/target_groups/{id}` (base URL `https://billetto.dk/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-target-group.md) for the provider-specific parameters and requirements.

