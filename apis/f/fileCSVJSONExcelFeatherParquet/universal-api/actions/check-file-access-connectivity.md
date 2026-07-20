# File (CSV, JSON, Excel, Feather, Parquet): Check File Access / Connectivity

Retrieves connectivity guidance for a file source.

```
GET https://connect.mindcloud.co/v1/universal/fileCSVJSONExcelFeatherParquet/latest/actions/check-file-access-connectivity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a File (CSV, JSON, Excel, Feather, Parquet) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileCSVJSONExcelFeatherParquet/latest/actions/check-file-access-connectivity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileCSVJSONExcelFeatherParquet/latest/actions/check-file-access-connectivity?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native File (CSV, JSON, Excel, Feather, Parquet) API returns.

## Native endpoint

Through the native File (CSV, JSON, Excel, Feather, Parquet) API, this operation is `GET /oss_registry.json` (base URL `https://connectors.airbyte.com/files/registries/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-file-access-connectivity.md) for the provider-specific parameters and requirements.

