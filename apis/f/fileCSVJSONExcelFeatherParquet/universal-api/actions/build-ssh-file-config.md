# File (CSV, JSON, Excel, Feather, Parquet): Build SSH File Config

Creates an SSH file source configuration.

```
POST https://connect.mindcloud.co/v1/universal/fileCSVJSONExcelFeatherParquet/latest/actions/build-ssh-file-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a File (CSV, JSON, Excel, Feather, Parquet) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fileCSVJSONExcelFeatherParquet/latest/actions/build-ssh-file-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fileCSVJSONExcelFeatherParquet/latest/actions/build-ssh-file-config', {
  method: 'POST',
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native File (CSV, JSON, Excel, Feather, Parquet) API returns.

## Native endpoint

Through the native File (CSV, JSON, Excel, Feather, Parquet) API, this operation is `GET /oss_registry.json` (base URL `https://connectors.airbyte.com/files/registries/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/build-ssh-file-config.md) for the provider-specific parameters and requirements.

