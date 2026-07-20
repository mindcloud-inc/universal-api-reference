# Mode: Get Collection Membership

Get details for a specific membership in a Mode collection.

```
GET https://connect.mindcloud.co/v1/universal/mode/latest/actions/get-collection-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mode/latest/actions/get-collection-membership?connectionId=$CONNECTION_ID&space=string&spaceMembership=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "space": "string",
  "spaceMembership": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mode/latest/actions/get-collection-membership?${params}`, {
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
| `space` | string | yes | Mode collection token. |
| `spaceMembership` | string | yes | Mode collection membership token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "Forms": {},
      "Links": {},
      "memberId": "Ava Chen",
      "memberToken": "string",
      "memberType": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Member email address. |
| `Forms` | object | Mode HAL forms. |
| `Links` | object | Mode HAL links. |
| `memberId` | string | Mode member identifier. |
| `memberToken` | string | Mode member token. |
| `memberType` | string | Mode member type. |
| `token` | string | Mode collection membership token. |

## Native endpoint

Through the native Mode API, this operation is `GET /spaces/[:space]/memberships/[:spaceMembership]` (base URL `https://app.mode.com/api/{{credentials.workspace}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection-membership.md) for the provider-specific parameters and requirements.

