# SigningHub: Delete Document

Deletes a document from SigningHub.

```
DELETE https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/delete-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/delete-document?connectionId=$CONNECTION_ID&packageId=11191608&documentId=13459159" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "11191608",
  "documentId": "13459159"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/delete-document?${params}`, {
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
| `packageId` | number | yes | The document package containing the document to delete. Example: `11191608`. |
| `documentId` | number | yes | The document to delete. Example: `13459159`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "package_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `package_name` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `DELETE /v4/packages/:packageId/documents/:documentId` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document.md) for the provider-specific parameters and requirements.

