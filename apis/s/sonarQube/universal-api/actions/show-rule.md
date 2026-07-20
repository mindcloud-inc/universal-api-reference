# SonarQube: Show Rule

Retrieves a rule from SonarQube.

```
GET https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/show-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SonarQube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/show-rule?connectionId=$CONNECTION_ID&key=string&organization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string",
  "organization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/show-rule?${params}`, {
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
| `key` | string | yes | Rule key. Required by /api/rules/show. |
| `organization` | string | yes | SonarCloud organization key. Required by /api/rules/show. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actives": {},
      "rule": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actives` | object |  |
| `rule` | object |  |

## Native endpoint

Through the native SonarQube API, this operation is `GET /api/rules/show` (base URL `https://sonarcloud.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-rule.md) for the provider-specific parameters and requirements.

