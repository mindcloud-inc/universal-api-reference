# Frappe: Delete Document V2

Deletes a document from a Frappe DocType.

```
DELETE https://connect.mindcloud.co/v1/universal/frappe/latest/actions/delete-document-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frappe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/frappe/latest/actions/delete-document-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frappe/latest/actions/delete-document-v2?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Delete confirmation returned by Frappe. |

## Native endpoint

Through the native Frappe API, this operation is `DELETE /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/` (base URL `{{credentials.siteUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document-v2.md) for the provider-specific parameters and requirements.

