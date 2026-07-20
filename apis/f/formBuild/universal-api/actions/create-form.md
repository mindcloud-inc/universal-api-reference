# 123FormBuild: Create Form

Creates a new form in 123FormBuilder.

```
POST https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 123FormBuild `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the new form |
| `groupId` | number | no | The ID of the group in which you want to create the form |
| `active` | number | no | Form activity status |
| `activeDateFrom` | date | no | Start date when active status is period-based |
| `activeDateTo` | date | no | End date when active status is period-based |
| `activeDays` | string | no | Comma-separated day numbers when active status is weekly |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 123FormBuild API returns.

## Native endpoint

Through the native 123FormBuild API, this operation is `POST /forms` (base URL `https://api.123formbuilder.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

