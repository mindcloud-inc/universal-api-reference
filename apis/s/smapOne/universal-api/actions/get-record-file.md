# smapOne: Get record file

Retrieves a record file from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-record-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-record-file?connectionId=$CONNECTION_ID&file_id=string&record_id=string&smap_id=string&version=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_id": "string",
  "record_id": "string",
  "smap_id": "string",
  "version": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-record-file?${params}`, {
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
| `file_id` | string | yes | The file id. |
| `record_id` | string | yes | The data record id. |
| `smap_id` | string | yes | The smap id. |
| `version` | string | yes | The smap version in major or major.minor format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native smapOne API returns.

## Native endpoint

Through the native smapOne API, this operation is `GET /v1/Smaps/{smapId}/Versions/{version}/Data/{recordId}/Files/{fileId}` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record-file.md) for the provider-specific parameters and requirements.

