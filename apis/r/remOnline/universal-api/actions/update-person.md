# RemOnline: Update Person

Updates an existing person in RemOnline.

```
PUT https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RemOnline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "person_id": "38077743"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "person_id": "38077743"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `person_id` | number | yes | ID of the person. Example: `38077743`. |
| `notes` | string | no | Notes text. Example: `Updated by MindCloud Stage3`. |
| `firstName` | string | no | Person first name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RemOnline API returns.

## Native endpoint

Through the native RemOnline API, this operation is `PATCH /v2/contacts/people/:person_id` (base URL `https://api.roapp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person.md) for the provider-specific parameters and requirements.

