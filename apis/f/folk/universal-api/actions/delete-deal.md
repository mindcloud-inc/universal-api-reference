# folk: Delete Deal

Deletes an existing deal from folk.

```
DELETE https://connect.mindcloud.co/v1/universal/folk/latest/actions/delete-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/folk/latest/actions/delete-deal?connectionId=$CONNECTION_ID&groupId=string&objectType=Deals&objectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string",
  "objectType": "Deals",
  "objectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/folk/latest/actions/delete-deal?${params}`, {
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
| `groupId` | string | yes | The group ID that owns the deal object field. |
| `objectType` | string | yes | The exact deal object type name from group custom fields, such as Deals. Default: `Deals`. |
| `objectId` | string | yes | The ID of the deal object to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native folk API, this operation is `DELETE /v1/groups/:groupId/:objectType/:objectId` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-deal.md) for the provider-specific parameters and requirements.

