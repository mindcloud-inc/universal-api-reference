# smapOne: Get datasource

Retrieves a data source from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-datasource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-datasource?connectionId=$CONNECTION_ID&data_source_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data_source_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-datasource?${params}`, {
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
      "dataSourceId": "string",
      "id": "string",
      "lastChanged": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataSourceId` | string |  |
| `id` | string |  |
| `lastChanged` | date |  |
| `title` | string |  |
| `version` | string |  |

## Native endpoint

Through the native smapOne API, this operation is `GET /intern/DataSource/{dataSourceId}` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datasource.md) for the provider-specific parameters and requirements.

