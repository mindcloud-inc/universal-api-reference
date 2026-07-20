# Affinda: List values for a data source

Retrieves values from an Affinda mapping data source.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-data-source-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-data-source-values?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-data-source-values?${params}`, {
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
| `annotation` | string | no | Filter based on annotation ID |
| `document` | string | no | Identifier of the document to apply filter lookups on if available |
| `identifier` | string | yes | Data source's identifier |
| `limit` | string | no | The numbers of results to return. |
| `offset` | string | no | The number of documents to skip before starting to collect the result set. |
| `search` | string | no | Search for specific values |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Affinda API returns.

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/mapping_data_sources/:identifier/values` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-source-values.md) for the provider-specific parameters and requirements.

