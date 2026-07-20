# Neon: Retrieve organization member details

Retrieves organization member details from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-organization-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-organization-member?connectionId=$CONNECTION_ID&org_id=string&member_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "org_id": "string",
  "member_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-organization-member?${params}`, {
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
| `org_id` | string | yes | Neon API parameter org_id |
| `member_id` | string | yes | Neon API parameter member_id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "joined_at": "2026-05-07T12:00:00.000Z",
      "org_id": "string",
      "role": [
        "string"
      ],
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `joined_at` | date |  |
| `org_id` | string |  |
| `role` | array |  |
| `user_id` | string |  |

## Native endpoint

Through the native Neon API, this operation is `GET /organizations/:org_id/members/:member_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-member.md) for the provider-specific parameters and requirements.

