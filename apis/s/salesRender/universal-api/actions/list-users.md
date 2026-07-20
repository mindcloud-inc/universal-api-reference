# SalesRender: List Users

Retrieves users from SalesRender.

```
GET https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesRender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-users?connectionId=$CONNECTION_ID&query=query%20%7B%20usersFetcher%20%7B%20users%20%7B%20id%20email%20registeredAt%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query { usersFetcher { users { id email registeredAt } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-users?${params}`, {
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
| `query` | string | yes | GraphQL query to execute against SalesRender. Default: `query {\n  usersFetcher {\n    users {\n      id\n      email\n      registeredAt\n    }\n  }\n}`. Example: `query { usersFetcher { users { id email registeredAt } } }`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | Optional GraphQL variables object. Default: `{}`. Example: `Optional JSON variables string`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "usersFetcher": {
          "users": [
            {
              "email": "ava@example.com",
              "id": "string",
              "registeredAt": "2026-05-07T12:00:00.000Z"
            }
          ]
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
| `data.usersFetcher.users[].email` | string | User email address. |
| `data.usersFetcher.users[].id` | string | User ID. |
| `data.usersFetcher.users[].registeredAt` | date | User registration timestamp. |

## Native endpoint

Through the native SalesRender API, this operation is `POST :companyId/CRM` (base URL `https://de.backend.salesrender.com/companies`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

