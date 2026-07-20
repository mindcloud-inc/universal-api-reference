# smapOne: Delete records

Deletes data records from a smapOne version.

```
DELETE https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/delete-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/delete-records?connectionId=$CONNECTION_ID&smap_id=string&version=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "smap_id": "string",
  "version": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/delete-records?${params}`, {
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
| `smap_id` | string | yes | The smap id. |
| `state` | string | no | Optional record state filter: new, exported, or incomplete. |
| `version` | string | yes | The smap version in major or major.minor format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedCount": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedCount` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native smapOne API, this operation is `DELETE /v1/Smaps/{smapId}/Versions/{version}/Data` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records.md) for the provider-specific parameters and requirements.

