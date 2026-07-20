# SigningHub: List Workflow Users

Retrieves workflow users from SigningHub.

```
GET https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/list-workflow-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/list-workflow-users?connectionId=$CONNECTION_ID&packageId=11191587" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "11191587"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/list-workflow-users?${params}`, {
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
| `packageId` | number | yes | The document package whose workflow users should be returned. Example: `11191587`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "delegatee": "string",
      "delegatee_name": "Ava Chen",
      "delivery_method": "string",
      "electronic_seal": {},
      "email_language_code": "ava@example.com",
      "gatekeepers": {},
      "group_members": [
        {}
      ],
      "group_name": "Ava Chen",
      "guest_user": true,
      "mobile_number": "string",
      "order": 1,
      "placeholder": "string",
      "process_status": "string",
      "processed_as": "string",
      "processed_by": "string",
      "processed_on": "string",
      "reason": "string",
      "role": "string",
      "signing_order": 1,
      "user_email": "ava@example.com",
      "user_name": "Ava Chen",
      "user_national_id": "string",
      "user_photo_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `delegatee` | string |  |
| `delegatee_name` | string |  |
| `delivery_method` | string |  |
| `electronic_seal` | object |  |
| `email_language_code` | string |  |
| `gatekeepers` | object |  |
| `group_members` | array<object> |  |
| `group_name` | string |  |
| `guest_user` | boolean |  |
| `mobile_number` | string |  |
| `order` | number |  |
| `placeholder` | string |  |
| `process_status` | string |  |
| `processed_as` | string |  |
| `processed_by` | string |  |
| `processed_on` | string |  |
| `reason` | string |  |
| `role` | string |  |
| `signing_order` | number |  |
| `user_email` | string |  |
| `user_name` | string |  |
| `user_national_id` | string |  |
| `user_photo_url` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `GET /v4/packages/:packageId/workflow/users` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-users.md) for the provider-specific parameters and requirements.

