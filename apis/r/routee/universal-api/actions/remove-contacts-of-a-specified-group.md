# Routee: Remove Contacts of a specified group

Removes contacts of a specified group in Routee.

```
DELETE https://connect.mindcloud.co/v1/universal/routee/latest/actions/remove-contacts-of-a-specified-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/routee/latest/actions/remove-contacts-of-a-specified-group?connectionId=$CONNECTION_ID&groupName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/remove-contacts-of-a-specified-group?${params}`, {
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
| `groupName` | string | yes | The name of the group which contains the contacts |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `size` | number |  |

## Native endpoint

Through the native Routee API, this operation is `DELETE /groups/my/:groupName/contacts` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contacts-of-a-specified-group.md) for the provider-specific parameters and requirements.

