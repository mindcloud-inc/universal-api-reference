# SonarQube: List Component Measures

Retrieves component measures from SonarQube.

```
GET https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/list-component-measures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SonarQube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/list-component-measures?connectionId=$CONNECTION_ID&component=string&metricKeys=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "component": "string",
  "metricKeys": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/list-component-measures?${params}`, {
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
| `component` | string | yes | Component key. Required by /api/measures/component_tree. |
| `metricKeys` | string | yes | Comma-separated metric keys. Required by /api/measures/component_tree. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseComponent": {},
      "components": [
        {}
      ],
      "metrics": [
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
| `baseComponent` | object |  |
| `components` | array<object> |  |
| `metrics` | array<object> |  |
| `paging` | object |  |

## Native endpoint

Through the native SonarQube API, this operation is `GET /api/measures/component_tree` (base URL `https://sonarcloud.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-component-measures.md) for the provider-specific parameters and requirements.

