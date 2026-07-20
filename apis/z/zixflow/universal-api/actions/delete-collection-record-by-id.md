# Zixflow: Delete Collection Record By ID

Deletes an existing collection record from Zixflow.

```
DELETE https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/delete-collection-record-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/delete-collection-record-by-id?connectionId=$CONNECTION_ID&collectionId=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/delete-collection-record-by-id?${params}`, {
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
| `collectionId` | string | yes | Collection identifier. |
| `recordId` | string | yes | Record identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the collection-record delete request succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `DELETE /collection-records/:collectionId/:recordId` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-collection-record-by-id.md) for the provider-specific parameters and requirements.

