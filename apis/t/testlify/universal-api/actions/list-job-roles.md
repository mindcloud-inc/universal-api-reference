# Testlify: List Job Roles

Retrieves job roles from the Testlify workspace.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-job-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-job-roles?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-job-roles?${params}`, {
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
| `q` | string | yes | Search text for job roles. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "id": "string",
      "isTemplateAvailable": true,
      "name": "Ava Chen",
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `id` | string |  |
| `isTemplateAvailable` | boolean |  |
| `name` | string |  |
| `score` | number |  |

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/workspace/jobrole` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-roles.md) for the provider-specific parameters and requirements.

