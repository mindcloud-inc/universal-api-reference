# SparrowDesk: List Members

Retrieves members from SparrowDesk.

```
GET https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "isCopilotSeatAlloted": true,
      "lastName": "Chen",
      "pages": {
        "perPage": 1
      },
      "phone": "string",
      "profilePic": "string",
      "role": {
        "id": 1,
        "label": "string"
      },
      "teams": [
        {}
      ],
      "totalCount": 1,
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Creation timestamp. |
| `email` | string | Member email address. |
| `firstName` | string | Member first name. |
| `id` | number | Member ID. |
| `isCopilotSeatAlloted` | boolean | Whether a Copilot seat is assigned. |
| `lastName` | string | Member last name. |
| `pages.perPage` | number | Page size. |
| `phone` | string | Member phone number. |
| `profilePic` | string | Member profile picture URL. |
| `role.id` | number | Role ID. |
| `role.label` | string | Role label. |
| `teams` | array<object> | Assigned teams. |
| `totalCount` | number | Total number of members. |
| `verified` | boolean | Whether the member is verified. |

## Native endpoint

Through the native SparrowDesk API, this operation is `GET /members` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

