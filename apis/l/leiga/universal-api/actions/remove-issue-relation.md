# Leiga: Remove Issue Relation

Deletes an existing issue relation from Leiga.

```
DELETE https://connect.mindcloud.co/v1/universal/leiga/latest/actions/remove-issue-relation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/remove-issue-relation?connectionId=$CONNECTION_ID&issueId=1&linkedIssueId=1&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "issueId": "1",
  "linkedIssueId": "1",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/remove-issue-relation?${params}`, {
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
| `issueId` | number | yes | Issue ID |
| `linkedIssueId` | number | yes | Related Issue ID |
| `type` | string | yes | Relation Type |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the relation removal succeeded. |

## Native endpoint

Through the native Leiga API, this operation is `POST /issue/remove-relationship` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-issue-relation.md) for the provider-specific parameters and requirements.

