# iLovePDF: Remove Uploaded File

Deletes an uploaded file from iLovePDF.

```
DELETE https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/remove-uploaded-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/remove-uploaded-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/remove-uploaded-file?${params}`, {
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
      "server_filename": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `server_filename` | string |  |

## Native endpoint

Through the native iLovePDF API, this operation is `DELETE https://:server/v1/upload/:task/:serverFilename` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-uploaded-file.md) for the provider-specific parameters and requirements.

