# Zillow MLS Data: List IDX field rules (OData)

Retrieves IDX field rules from Zillow MLS Data using OData.

```
GET https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-idx-field-rules-o-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow MLS Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-idx-field-rules-o-data?connectionId=$CONNECTION_ID&dataset=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-idx-field-rules-o-data?${params}`, {
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
| `dataset` | string | yes | Bridge dataset code that scopes the OData IDX field rules query. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zillow MLS Data API returns.

## Native endpoint

Through the native Zillow MLS Data API, this operation is `GET /OData/:dataset/idx/Field` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-idx-field-rules-o-data.md) for the provider-specific parameters and requirements.

