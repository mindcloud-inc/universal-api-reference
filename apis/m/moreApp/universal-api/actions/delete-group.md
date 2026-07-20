# MoreApp: Delete Group

Deletes a group from MoreApp.

```
DELETE https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/delete-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/delete-group?connectionId=$CONNECTION_ID&customerId=209321&groupId=69bc4c7a0e76586ace7d82bd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "209321",
  "groupId": "69bc4c7a0e76586ace7d82bd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/delete-group?${params}`, {
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
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `groupId` | string | yes | MoreApp group identifier. Default: `69bc4c7a0e76586ace7d82bd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externallyManaged": true,
      "grants": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externallyManaged` | boolean |  |
| `grants` | array<object> |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `DELETE /api/v2/customers/{{customerId}}/groups/{{groupId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-group.md) for the provider-specific parameters and requirements.

