# smapOne: List record files

Retrieves record file metadata from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-record-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-record-files?connectionId=$CONNECTION_ID&record_id=string&smap_id=string&version=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "record_id": "string",
  "smap_id": "string",
  "version": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-record-files?${params}`, {
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
| `record_id` | string | yes | The data record id. |
| `smap_id` | string | yes | The smap id. |
| `version` | string | yes | The smap version in major or major.minor format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "fileId": "string",
      "fileName": "Ava Chen",
      "id": "string",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `fileId` | string |  |
| `fileName` | string |  |
| `id` | string |  |
| `size` | number |  |

## Native endpoint

Through the native smapOne API, this operation is `GET /v1/Smaps/{smapId}/Versions/{version}/Data/{recordId}/Files` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-record-files.md) for the provider-specific parameters and requirements.

