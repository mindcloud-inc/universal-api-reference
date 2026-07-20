# Form.io: Create Admin Submission

Creates a new admin submission in your Form.io project.

```
POST https://connect.mindcloud.co/v1/universal/formio/latest/actions/create-admin-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formio/latest/actions/create-admin-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formio/latest/actions/create-admin-submission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email stored on the admin submission. |
| `password` | string | yes | Password stored on the admin submission. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "created": "string",
      "data": {},
      "form": "string",
      "modified": "string",
      "owner": "string",
      "project": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `created` | string |  |
| `data` | object |  |
| `form` | string |  |
| `modified` | string |  |
| `owner` | string |  |
| `project` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Form.io API, this operation is `POST /admin/submission` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-admin-submission.md) for the provider-specific parameters and requirements.

