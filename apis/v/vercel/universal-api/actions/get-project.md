# Vercel: Get Project

Retrieves a project record from Vercel.

```
GET https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-project?connectionId=$CONNECTION_ID&idOrName=prj_1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "prj_1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-project?${params}`, {
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
| `idOrName` | string | yes | The unique project identifier or the project name Example: `prj_1234567890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "createdAt": 1,
      "id": "string",
      "live": true,
      "name": "Ava Chen",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | The owning account identifier |
| `createdAt` | number | Project creation timestamp |
| `id` | string | The project identifier |
| `live` | boolean | Whether the project is live |
| `name` | string | The project name |
| `updatedAt` | number | Project update timestamp |

## Native endpoint

Through the native Vercel API, this operation is `GET /v9/projects/:idOrName` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

