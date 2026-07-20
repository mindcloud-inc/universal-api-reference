# Leiga: List Issue Relations

Retrieves issue relations for an issue in Leiga.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-issue-relations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-issue-relations?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-issue-relations?${params}`, {
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
| `id` | number | yes | Issue ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "issueId": 1,
      "projectId": 1,
      "summary": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `issueId` | number | Related issue ID. |
| `projectId` | number | Project ID. |
| `summary` | string | Related issue summary. |
| `type` | string | Relation type. |

## Native endpoint

Through the native Leiga API, this operation is `GET /issue/relationship-list` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-issue-relations.md) for the provider-specific parameters and requirements.

