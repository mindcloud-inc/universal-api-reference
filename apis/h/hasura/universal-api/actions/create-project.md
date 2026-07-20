# Hasura: Create Project

Creates a new project in Hasura Cloud.

```
POST https://connect.mindcloud.co/v1/universal/hasura/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hasura `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hasura/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloud": "aws",
  "region": "us-east-2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hasura/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloud": "aws",
    "region": "us-east-2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cloud` | string | yes | Hasura Cloud provider identifier, for example aws. Default: `aws`. |
| `region` | string | yes | Cloud region for the project, for example us-east-2. Default: `us-east-2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `envs[]` | array<object> | no | Optional environment variables as objects with key and value fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createTenant": {
          "id": "string",
          "name": "Ava Chen",
          "tenant": {
            "id": "string",
            "project": {
              "endpoint": "string",
              "id": "string",
              "name": "Ava Chen"
            },
            "slug": "string"
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createTenant.id` | string | Created project ID. |
| `data.createTenant.name` | string | Created project name. |
| `data.createTenant.tenant.id` | string | Created tenant ID. |
| `data.createTenant.tenant.project.endpoint` | string | Created project endpoint. |
| `data.createTenant.tenant.project.id` | string | Created tenant project ID. |
| `data.createTenant.tenant.project.name` | string | Created tenant project name. |
| `data.createTenant.tenant.slug` | string | Created tenant slug. |

## Native endpoint

Through the native Hasura API, this operation is `POST /v1/graphql` (base URL `https://data.pro.hasura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

