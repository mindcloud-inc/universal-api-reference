# Vercel: List Project Env Vars

Retrieves project environment variables from Vercel.

```
GET https://connect.mindcloud.co/v1/universal/vercel/latest/actions/list-project-env-vars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/list-project-env-vars?connectionId=$CONNECTION_ID&idOrName=prj_1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "prj_1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/list-project-env-vars?${params}`, {
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
      "envs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `envs` | array<object> | The project environment variables |

## Native endpoint

Through the native Vercel API, this operation is `GET /v10/projects/:idOrName/env` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-env-vars.md) for the provider-specific parameters and requirements.

