# Leiga: Get Issue Scheme

Retrieves an issue scheme from Leiga.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-issue-scheme
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-issue-scheme?connectionId=$CONNECTION_ID&issueTypeId=1&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "issueTypeId": "1",
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-issue-scheme?${params}`, {
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
| `issueTypeId` | number | yes | Issue Type ID |
| `projectId` | number | yes | Project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {}
      ],
      "issueTypeId": 1,
      "projectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | array<object> |  |
| `issueTypeId` | number |  |
| `projectId` | number |  |

## Native endpoint

Through the native Leiga API, this operation is `GET /issue/issue-scheme` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issue-scheme.md) for the provider-specific parameters and requirements.

