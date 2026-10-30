# GoCanvas: Update Project



```
PUT https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | Identifier of the project to update. |
| `name` | string | no | Project name; PATCH documentation conflicts on whether it is required. |
| `departmentId` | number | no | Department associated with the project. |
| `customerId` | number | no | Customer associated with the project; the documentation example sends null. |
| `siteId` | number | no | Site associated with the customer; the documentation example sends null. |
| `startDate` | string | no | Project start date or datetime in ISO 8601 format. |
| `endDate` | string | no | Project end date or datetime in ISO 8601 format. |
| `status` | list | no | Project status. One of: `active`, `draft`, `inactive`. |
| `notes` | string | no | Longer description of the project. |
| `code` | string | no | Alphanumeric code uniquely identifying the project. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoCanvas API returns.

## Native endpoint

Through the native GoCanvas API, this operation is `PATCH /projects/:projectId` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

