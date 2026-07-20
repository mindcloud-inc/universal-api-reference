# TalentLyft: Create Department

Creates a new department in TalentLyft.

```
POST https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/create-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLyft `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/create-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/create-department', {
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
| `name` | string | yes | The department name. |
| `externalId` | string | no | Optional external identifier for the department. |
| `parentId` | number | no | Optional parent department ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TalentLyft API returns.

## Native endpoint

Through the native TalentLyft API, this operation is `POST /v2/departments` (base URL `https://api.talentlyft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-department.md) for the provider-specific parameters and requirements.

