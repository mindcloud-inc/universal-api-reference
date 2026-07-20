# GrowthBook: Get a Data Source's Information Schema

Retrieves a data source information schema from GrowthBook.

```
GET https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-information-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-information-schema?connectionId=$CONNECTION_ID&dataSourceId=data_source_1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataSourceId": "data_source_1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-information-schema?${params}`, {
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
| `dataSourceId` | string | yes | The id of the data source Default: `data_source_1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "informationSchema": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `informationSchema` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `GET /data-sources/:dataSourceId/information-schema` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-information-schema.md) for the provider-specific parameters and requirements.

