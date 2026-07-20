# OpenSanctions: Match Entity By Example



```
GET https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/match-entity-by-example
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSanctions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/match-entity-by-example?connectionId=$CONNECTION_ID&dataset=default&queries=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "default",
  "queries": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/match-entity-by-example?${params}`, {
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
| `dataset` | string | yes | Data source or collection name to scope the match query to. Use default to match against the full OpenSanctions dataset. Default: `default`. |
| `queries` | object | yes | Object of named entity examples to match. Each value must include schema and properties according to the EntityExample schema. Default: `{"putin":{"schema":"Person","properties":{"name":["Vladimir Putin"],"birthDate":["1952-10-07"]}}}`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threshold` | number | no | Score threshold for results to be considered matches. Default: `0.7`. |
| `algorithm` | string | no | Scoring algorithm to use. The API defines best as the default algorithm. Default: `best`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limit": 1,
      "responses": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number | Number of match candidates returned per query. |
| `responses` | object | Object keyed by query name containing match results and totals. |

## Native endpoint

Through the native OpenSanctions API, this operation is `POST /match/:dataset` (base URL `https://api.opensanctions.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/match-entity-by-example.md) for the provider-specific parameters and requirements.

