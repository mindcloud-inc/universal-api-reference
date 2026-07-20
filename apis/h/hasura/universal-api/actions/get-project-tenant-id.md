# Hasura: Get Project Tenant ID

Retrieves a Hasura project tenant ID.

```
GET https://connect.mindcloud.co/v1/universal/hasura/latest/actions/get-project-tenant-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hasura `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasura/latest/actions/get-project-tenant-id?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasura/latest/actions/get-project-tenant-id?${params}`, {
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
| `projectId` | string | yes | Hasura Cloud project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "projects_by_pk": {
          "id": "string",
          "tenant": {
            "id": "string"
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
| `data.projects_by_pk.id` | string | Project ID. |
| `data.projects_by_pk.tenant.id` | string | Tenant ID associated with the project. |

## Native endpoint

Through the native Hasura API, this operation is `POST /v1/graphql` (base URL `https://data.pro.hasura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-tenant-id.md) for the provider-specific parameters and requirements.

