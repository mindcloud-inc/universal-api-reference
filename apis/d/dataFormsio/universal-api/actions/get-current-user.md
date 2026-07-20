# DataForms.io: Get Current User

Retrieves the current user from DataForms.io.

```
GET https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForms.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "companyId": "string",
        "createdAt": "string",
        "email": "ava@example.com",
        "firstname": "Ava",
        "id": "string",
        "lastname": "Chen",
        "locale": "string",
        "roleId": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.companyId` | string |  |
| `data.createdAt` | string |  |
| `data.email` | string |  |
| `data.firstname` | string |  |
| `data.id` | string |  |
| `data.lastname` | string |  |
| `data.locale` | string |  |
| `data.roleId` | string |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native DataForms.io API, this operation is `GET /user` (base URL `https://api.dataforms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

