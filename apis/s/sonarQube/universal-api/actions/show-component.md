# SonarQube: Show Component

Retrieves a component from SonarQube.

```
GET https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/show-component
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SonarQube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/show-component?connectionId=$CONNECTION_ID&component=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "component": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/show-component?${params}`, {
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
| `component` | string | yes | Component key to show. Required by /api/components/show. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ancestors": [
        {}
      ],
      "component": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ancestors` | array<object> |  |
| `component` | object |  |

## Native endpoint

Through the native SonarQube API, this operation is `GET /api/components/show` (base URL `https://sonarcloud.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-component.md) for the provider-specific parameters and requirements.

