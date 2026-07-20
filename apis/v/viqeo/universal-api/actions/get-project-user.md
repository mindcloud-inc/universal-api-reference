# Viqeo: Get Project User

Retrieves a project user from Viqeo.

```
GET https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/get-project-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viqeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/get-project-user?connectionId=$CONNECTION_ID&projectId=string&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/get-project-user?${params}`, {
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
| `projectId` | string | yes | Project identifier from the path. |
| `email` | string | yes | Project user email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "locale": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Project user email address. |
| `locale` | string | Project user locale. |

## Native endpoint

Through the native Viqeo API, this operation is `GET /media-platform/v1/project/:projectId/user/:email` (base URL `https://api.viqeo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-user.md) for the provider-specific parameters and requirements.

