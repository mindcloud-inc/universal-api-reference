# Clappia: Add User to Workplace

Creates a new workplace user in Clappia.

```
POST https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-user-to-workplace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-user-to-workplace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-user-to-workplace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailAddress` | string | no | Email address of the workplace user to add. |
| `phoneNumber` | string | no | Phone number of the workplace user to add. |
| `attributes` | object | no | Optional attribute object to assign when adding the user. |
| `groupNames[]` | array<string> | no | Optional group names to assign when adding the user. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clappia API returns.

## Native endpoint

Through the native Clappia API, this operation is `POST /workplace/addUserToWorkplace` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-workplace.md) for the provider-specific parameters and requirements.

