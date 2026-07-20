# Neon: Retrieve organization members details

Retrieves organization members from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-organization-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-organization-members?connectionId=$CONNECTION_ID&org_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "org_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-organization-members?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort_by` | list | no | Neon API parameter sort_by One of: `0`, `1`, `2`. |
| `sort_order` | list | no | Neon API parameter sort_order One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "members": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `members` | array<object> |  |
| `pagination` | object |  |

## Native endpoint

Through the native Neon API, this operation is `GET /organizations/:org_id/members` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-members.md) for the provider-specific parameters and requirements.

