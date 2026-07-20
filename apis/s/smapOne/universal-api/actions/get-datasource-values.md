# smapOne: Get datasource values

Retrieves data source values from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-datasource-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-datasource-values?connectionId=$CONNECTION_ID&data_source_id=string&data_source_version=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data_source_id": "string",
  "data_source_version": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-datasource-values?${params}`, {
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
| `data_source_version` | string | yes | The datasource version number, for example 1.0. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "title": "string",
      "value": "string",
      "values": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `title` | string |  |
| `value` | string |  |
| `values` | array<object> |  |

## Native endpoint

Through the native smapOne API, this operation is `GET /intern/DataSource/{dataSourceId}/Versions/{dataSourceVersion}/Definition/Values` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datasource-values.md) for the provider-specific parameters and requirements.

