# SonarQube: Search Measure History

Finds measure history in SonarQube.

```
GET https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/search-measure-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SonarQube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/search-measure-history?connectionId=$CONNECTION_ID&component=string&component=string&metrics=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "component": "string",
  "component": "string",
  "metrics": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/search-measure-history?${params}`, {
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
| `component` | string | yes | Component key. Required by /api/measures/search_history. |
| `component` | string | yes | Component key. Required by /api/measures/search_history. |
| `metrics` | string | yes | Comma-separated metric keys. Required by /api/measures/search_history. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "measures": [
        {}
      ],
      "paging": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `measures` | array<object> |  |
| `paging` | object |  |

## Native endpoint

Through the native SonarQube API, this operation is `GET /api/measures/search_history` (base URL `https://sonarcloud.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-measure-history.md) for the provider-specific parameters and requirements.

