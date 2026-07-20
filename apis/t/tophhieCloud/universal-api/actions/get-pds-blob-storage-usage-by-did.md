# Tophhie Cloud: Get PDS Blob Storage Usage By DID

Retrieves PDS blob storage usage by DID from Tophhie Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-pds-blob-storage-usage-by-did
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tophhie Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-pds-blob-storage-usage-by-did?connectionId=$CONNECTION_ID&did=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "did": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-pds-blob-storage-usage-by-did?${params}`, {
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
| `did` | string | yes | The decentralized identifier for the PDS repository. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blobCount": 1,
      "usageBytes": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blobCount` | number | Number of blobs when returned. |
| `usageBytes` | string | Blob storage usage in bytes for the DID. |

## Native endpoint

Through the native Tophhie Cloud API, this operation is `GET /pds/blobStorageUsageBytes/{did}` (base URL `https://api.tophhie.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pds-blob-storage-usage-by-did.md) for the provider-specific parameters and requirements.

