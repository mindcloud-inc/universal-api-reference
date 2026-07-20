# Timewax: List Project Activities

Retrieves all project activities from Timewax.

```
GET https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-project-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-project-activities?connectionId=$CONNECTION_ID&request.project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-project-activities?${params}`, {
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

Through the native Timewax API, this operation is `POST project/breakdown/list/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-activities.md) for the provider-specific parameters and requirements.

