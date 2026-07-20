# Windsor.ai: Get Connector Data

Retrieves report data from one Windsor.ai connector.

```
GET https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/get-connector-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Windsor.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/get-connector-data?connectionId=$CONNECTION_ID&connector=string&fields=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connector": "string",
  "fields": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/get-connector-data?${params}`, {
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
| `connector` | string | yes | Connector ID such as facebook or googleanalytics4. |
| `datePreset` | string | no | Relative date window such as last_7d or last_30d. |
| `fields` | string | yes | Comma-separated list of Windsor.ai fields to retrieve. |
| `filter` | string | no | JSON filter expression for Windsor.ai connector queries. |
| `maxRows` | number | no | Maximum number of rows to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Windsor.ai API returns.

## Native endpoint

Through the native Windsor.ai API, this operation is `GET https://connectors.windsor.ai/:connector` (base URL `https://onboard.windsor.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connector-data.md) for the provider-specific parameters and requirements.

