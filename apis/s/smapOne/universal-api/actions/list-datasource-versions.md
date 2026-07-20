# smapOne: List datasource versions

Retrieves data source versions from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-datasource-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-datasource-versions?connectionId=$CONNECTION_ID&data_source_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data_source_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-datasource-versions?${params}`, {
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
| `data_source_id` | string | yes | The datasource id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataCount": 1,
      "dataSourceVersion": "string",
      "lastChanged": "2026-05-07T12:00:00.000Z",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataCount` | number |  |
| `dataSourceVersion` | string |  |
| `lastChanged` | date |  |
| `version` | string |  |

## Native endpoint

Through the native smapOne API, this operation is `GET /intern/DataSource/{dataSourceId}/Versions` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datasource-versions.md) for the provider-specific parameters and requirements.

