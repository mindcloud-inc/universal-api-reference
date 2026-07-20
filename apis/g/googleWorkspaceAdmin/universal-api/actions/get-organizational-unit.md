# Google Workspace Admin: Get Organizational Unit

Retrieves an organizational unit from Google Workspace Admin.

```
GET https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/get-organizational-unit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/get-organizational-unit?connectionId=$CONNECTION_ID&customerId=my_customer&orgUnitPath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "my_customer",
  "orgUnitPath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/get-organizational-unit?${params}`, {
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
| `orgUnitPath` | string | yes | Full org unit path without the leading slash, or the org unit ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "etag": "string",
      "kind": "string",
      "name": "Ava Chen",
      "orgUnitId": "string",
      "orgUnitPath": "string",
      "parentOrgUnitId": "string",
      "parentOrgUnitPath": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `etag` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `orgUnitId` | string |  |
| `orgUnitPath` | string |  |
| `parentOrgUnitId` | string |  |
| `parentOrgUnitPath` | string |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `GET /admin/directory/v1/customer/:customerId/orgunits/:orgUnitPath` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organizational-unit.md) for the provider-specific parameters and requirements.

