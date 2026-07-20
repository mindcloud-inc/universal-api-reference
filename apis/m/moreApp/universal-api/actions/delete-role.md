# MoreApp: Delete Role

Deletes a role from MoreApp.

```
DELETE https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/delete-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/delete-role?connectionId=$CONNECTION_ID&customerId=1&roleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "roleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/delete-role?${params}`, {
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
| `customerId` | number | yes |  |
| `roleId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {},
      "message": "string",
      "traceId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `data` | object |  |
| `message` | string |  |
| `traceId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `DELETE /api/v2/customers/{{customerId}}/roles/{{roleId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-role.md) for the provider-specific parameters and requirements.

