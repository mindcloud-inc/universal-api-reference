# BrowserAct: List Official Workflow Templates

Retrieves official workflow templates from BrowserAct.

```
GET https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/list-official-workflow-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BrowserAct `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/list-official-workflow-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/list-official-workflow-templates?${params}`, {
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
| `keyword` | string | no | Optional search keyword for filtering official workflow templates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detailUrl": "https://example.com",
      "name": "Ava Chen",
      "recommendDesc": "string",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detailUrl` | string |  |
| `name` | string |  |
| `recommendDesc` | string |  |
| `templateId` | string |  |

## Native endpoint

Through the native BrowserAct API, this operation is `GET /list-official-workflow-templates` (base URL `https://api.browseract.com/v2/workflow`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-official-workflow-templates.md) for the provider-specific parameters and requirements.

