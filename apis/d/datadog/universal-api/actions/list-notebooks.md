# Datadog: List Notebooks

Retrieves notebooks from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-notebooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-notebooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-notebooks?${params}`, {
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
| `authorHandle` | string | no | Return notebooks created by this author handle. |
| `excludeAuthorHandle` | string | no | Exclude notebooks by author handle. |
| `count` | number | no | Number of notebooks to return. |
| `start` | number | no | Index of the first notebook to return. |
| `sortField` | string | no | Field to sort notebooks by. |
| `sortDir` | string | no | Direction for notebook sorting. |
| `query` | string | no | Search notebooks by name or author handle. |
| `includeCells` | boolean | no | Whether to include cells and global time in notebook results. |
| `isTemplate` | boolean | no | Return only template notebooks when true. |
| `type` | string | no | Notebook metadata type filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Notebook definitions returned by the request. |
| `meta` | object | Metadata returned by the notebooks API. |

## Native endpoint

Through the native Datadog API, this operation is `GET /api/v1/notebooks` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notebooks.md) for the provider-specific parameters and requirements.

