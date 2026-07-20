# Google Workspace Admin: Check Group Membership

Checks whether a user belongs to a group in Google Workspace Admin.

```
GET https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/check-group-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/check-group-membership?connectionId=$CONNECTION_ID&groupKey=string&memberKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupKey": "string",
  "memberKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/check-group-membership?${params}`, {
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
| `groupKey` | string | yes | Group email address, alias, or unique ID. |
| `memberKey` | string | yes | Member email address, alias, or unique ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isMember": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isMember` | boolean |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `GET /admin/directory/v1/groups/:groupKey/hasMember/:memberKey` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-group-membership.md) for the provider-specific parameters and requirements.

