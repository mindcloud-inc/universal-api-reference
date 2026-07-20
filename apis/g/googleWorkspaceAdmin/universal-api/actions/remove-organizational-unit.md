# Google Workspace Admin: Remove Organizational Unit

Deletes an organizational unit from Google Workspace Admin.

```
DELETE https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/remove-organizational-unit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/remove-organizational-unit?connectionId=$CONNECTION_ID&customerId=my_customer&orgUnitPath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "my_customer",
  "orgUnitPath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/remove-organizational-unit?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Workspace Admin API returns.

## Native endpoint

Through the native Google Workspace Admin API, this operation is `DELETE /admin/directory/v1/customer/:customerId/orgunits/:orgUnitPath` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-organizational-unit.md) for the provider-specific parameters and requirements.

