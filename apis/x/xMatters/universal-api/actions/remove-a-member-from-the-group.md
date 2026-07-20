# xMatters: Remove a member from the group

Removes a member from the group from your xMatters instance.

```
DELETE https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/remove-a-member-from-the-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/remove-a-member-from-the-group?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/remove-a-member-from-the-group?${params}`, {
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
| `groupId` | string | no |  |
| `memberId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "group": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "targetName": "Ava Chen"
      },
      "member": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group.id` | string |  |
| `group.links.self` | string |  |
| `group.targetName` | string |  |
| `member.id` | string |  |
| `member.links.self` | string |  |
| `member.recipientType` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `DELETE groups/{groupId}/members/{memberId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-a-member-from-the-group.md) for the provider-specific parameters and requirements.

