# DataBridge: Delete Document

Deletes a document from DataBridge.

```
DELETE https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/delete-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataBridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/delete-document?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/delete-document?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native DataBridge API, this operation is `DELETE /documents/:document_id` (base URL `https://api.morphik.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document.md) for the provider-specific parameters and requirements.

