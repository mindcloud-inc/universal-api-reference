# TalentLyft: Update Department

Updates an existing department in TalentLyft.

```
PUT https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/update-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLyft `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/update-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/update-department', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The TalentLyft department ID. |
| `name` | string | no | The new department name. |
| `externalId` | string | no | Optional external identifier for the department. |
| `parentId` | number | no | Optional parent department ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TalentLyft API returns.

## Native endpoint

Through the native TalentLyft API, this operation is `PUT /v2/departments/:id` (base URL `https://api.talentlyft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-department.md) for the provider-specific parameters and requirements.

