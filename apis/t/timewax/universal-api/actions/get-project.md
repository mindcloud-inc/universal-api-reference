# Timewax: Get Project

Retrieves a project from Timewax.

```
GET https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-project?connectionId=$CONNECTION_ID&request.project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-project?${params}`, {
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
| `request.project` | string | yes | Required. Project code or name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "company": "string",
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
| `code` | string | Project code. |
| `company` | string | Client or company associated with the project. |
| `name` | string | Project name. |
| `status` | string | Project status. |

## Native endpoint

Through the native Timewax API, this operation is `POST project/get/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

