# Federal Communications Commission: Move File

Moves an FCC OPIF file to a new folder.

```
PUT https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/move-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/move-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/move-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "entityId": "string",
      "fileId": "string",
      "newFolderId": "string",
      "serviceCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entityId` | string | FCC entity identifier. |
| `fileId` | string | File identifier. |
| `newFolderId` | string | Destination folder identifier. |
| `serviceCode` | string | FCC service code. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `PUT /api/manager/file/move.{format}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-file.md) for the provider-specific parameters and requirements.

