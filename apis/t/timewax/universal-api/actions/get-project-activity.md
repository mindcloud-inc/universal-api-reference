# Timewax: Get Project Activity

Retrieves a project activity from Timewax.

```
GET https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-project-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-project-activity?connectionId=$CONNECTION_ID&request.project=string&request.breakdown=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.project": "string",
  "request.breakdown": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-project-activity?${params}`, {
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
| `request.project` | string | yes | Required. Code or name of the project. |
| `request.breakdown` | string | yes | Required. Code or name of the activity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Activity code. |
| `name` | string | Activity name. |
| `status` | string | Activity status. |

## Native endpoint

Through the native Timewax API, this operation is `POST project/breakdown/get/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-activity.md) for the provider-specific parameters and requirements.

