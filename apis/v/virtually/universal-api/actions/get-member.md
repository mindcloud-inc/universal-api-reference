# Virtually: Get Member

Retrieves a member from your Virtually workspace.

```
GET https://connect.mindcloud.co/v1/universal/virtually/latest/actions/get-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/get-member?connectionId=$CONNECTION_ID&memberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "memberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/virtually/latest/actions/get-member?${params}`, {
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
| `memberId` | string | yes | The member ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "imageUri": {},
      "memberId": "string",
      "name": "Ava Chen",
      "notes": {},
      "role": "string",
      "timezone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `imageUri` | object |  |
| `memberId` | string |  |
| `name` | string |  |
| `notes` | object |  |
| `role` | string |  |
| `timezone` | object |  |

## Native endpoint

Through the native Virtually API, this operation is `GET /api/v2/orgs/:orgId/members/:memberId` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member.md) for the provider-specific parameters and requirements.

