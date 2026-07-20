# SonarQube: List Rule Tags

Retrieves rule tags from SonarQube.

```
GET https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/list-rule-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SonarQube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/list-rule-tags?connectionId=$CONNECTION_ID&organization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/list-rule-tags?${params}`, {
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
| `organization` | string | yes | SonarCloud organization key. Required by /api/rules/tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tags` | array<string> |  |

## Native endpoint

Through the native SonarQube API, this operation is `GET /api/rules/tags` (base URL `https://sonarcloud.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rule-tags.md) for the provider-specific parameters and requirements.

