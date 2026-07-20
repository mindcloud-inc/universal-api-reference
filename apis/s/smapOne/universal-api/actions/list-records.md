# smapOne: List records

Retrieves data records from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-records?connectionId=$CONNECTION_ID&smap_id=string&version=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "smap_id": "string",
  "version": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-records?${params}`, {
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
| `format` | string | no | Optional output format such as json or xml. |
| `smap_id` | string | yes | The smap id. |
| `state` | string | no | Optional record state filter: new, exported, or incomplete. |
| `version` | string | yes | The smap version in major or major.minor format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "recordType": "string",
      "userEmail": "ava@example.com",
      "userName": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `id` | string |  |
| `recordType` | string |  |
| `userEmail` | string |  |
| `userName` | string |  |
| `version` | string |  |

## Native endpoint

Through the native smapOne API, this operation is `GET /v1/Smaps/{smapId}/Versions/{version}/Data` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.

