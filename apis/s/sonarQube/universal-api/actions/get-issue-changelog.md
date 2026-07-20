# SonarQube: Get Issue Changelog

Retrieves an issue changelog from SonarQube.

```
GET https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/get-issue-changelog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SonarQube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/get-issue-changelog?connectionId=$CONNECTION_ID&issue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "issue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/get-issue-changelog?${params}`, {
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
| `issue` | string | yes | Issue key whose changelog should be returned. Required by /api/issues/changelog. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changelog": [
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
| `changelog` | array<object> |  |

## Native endpoint

Through the native SonarQube API, this operation is `GET /api/issues/changelog` (base URL `https://sonarcloud.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issue-changelog.md) for the provider-specific parameters and requirements.

