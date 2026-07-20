# GitScrum: Get Task by Code

Retrieves a GitScrum task by code.

```
GET https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-task-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitScrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-task-by-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-task-by-code?${params}`, {
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
| `code` | string | no |  |
| `companySlug` | string | no |  |
| `projectSlug` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "title": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `title` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native GitScrum API, this operation is `GET /tasks/by-code/:code` (base URL `https://services.gitscrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-by-code.md) for the provider-specific parameters and requirements.

