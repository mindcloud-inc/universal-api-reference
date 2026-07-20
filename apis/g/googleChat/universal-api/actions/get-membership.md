# Google Chat: Get Membership

Retrieves details about a Google Chat membership.

```
GET https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/get-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/get-membership?connectionId=$CONNECTION_ID&space=4Oe1TyAAAAE&member=1234567890%20or%20user%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "space": "4Oe1TyAAAAE",
  "member": "1234567890 or user@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/get-membership?${params}`, {
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
| `space` | string | yes | Enter only the space ID. If a membership name is spaces/4Oe1TyAAAAE/members/1234567890, enter 4Oe1TyAAAAE here. Example: `4Oe1TyAAAAE`. |
| `member` | string | yes | Enter the member identifier from the membership resource, or the user's email address when supported. If the membership name is spaces/4Oe1TyAAAAE/members/1234567890, enter 1234567890 here. Example: `1234567890 or user@example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Chat API returns.

## Native endpoint

Through the native Google Chat API, this operation is `GET /spaces/:space/members/:member` (base URL `https://chat.googleapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-membership.md) for the provider-specific parameters and requirements.

