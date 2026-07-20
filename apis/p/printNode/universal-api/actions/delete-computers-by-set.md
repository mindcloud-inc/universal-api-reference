# PrintNode: Delete Computers by Set

Deletes specific computers from PrintNode by ID set.

```
DELETE https://connect.mindcloud.co/v1/universal/printNode/latest/actions/delete-computers-by-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/delete-computers-by-set?connectionId=$CONNECTION_ID&computerSet=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "computerSet": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printNode/latest/actions/delete-computers-by-set?${params}`, {
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
| `computerSet` | string | yes | Comma-separated PrintNode computer IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | array<number> | IDs of the computers affected by the delete request. |

## Native endpoint

Through the native PrintNode API, this operation is `DELETE /computers/:computerSet` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-computers-by-set.md) for the provider-specific parameters and requirements.

