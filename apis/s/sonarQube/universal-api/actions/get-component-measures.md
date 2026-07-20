# SonarQube: Get Component Measures

Retrieves component measures from SonarQube.

```
GET https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/get-component-measures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SonarQube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/get-component-measures?connectionId=$CONNECTION_ID&component=string&metricKeys=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "component": "string",
  "metricKeys": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/get-component-measures?${params}`, {
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
| `component` | string | yes | Component key. Required by /api/measures/component. |
| `metricKeys` | string | yes | Comma-separated metric keys. Required by /api/measures/component. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "component": {},
      "metrics": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `component` | object |  |
| `metrics` | array<object> |  |

## Native endpoint

Through the native SonarQube API, this operation is `GET /api/measures/component` (base URL `https://sonarcloud.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-component-measures.md) for the provider-specific parameters and requirements.

