# Google Workspace Admin: List Organizational Units

Retrieves organizational units from Google Workspace Admin.

```
GET https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-organizational-units
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-organizational-units?connectionId=$CONNECTION_ID&customerId=my_customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "my_customer"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-organizational-units?${params}`, {
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
| `customerId` | string | yes | Workspace customer identifier. Use my_customer for the current tenant. Default: `my_customer`. |
| `orgUnitPath` | string | no | Optional parent organizational unit path to list from. |
| `type` | string | no | Whether to return children only or all nested org units. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "kind": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `kind` | string |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `GET /admin/directory/v1/customer/:customerId/orgunits` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizational-units.md) for the provider-specific parameters and requirements.

