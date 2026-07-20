# Mighty Networks: Remove Space Member

Removes a member from a space in Mighty Networks.

```
DELETE https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/remove-space-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/remove-space-member?connectionId=$CONNECTION_ID&networkId=%7B%7Bcredentials.networkId%7D%7D&spaceId=23049325&userId=38689843" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "networkId": "{{credentials.networkId}}",
  "spaceId": "23049325",
  "userId": "38689843"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/remove-space-member?${params}`, {
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
| `networkId` | string | yes | The Mighty Networks network ID or subdomain for the request path. Default: `{{credentials.networkId}}`. |
| `spaceId` | number | yes | ID of the space. Example: `23049325`. |
| `userId` | number | yes | ID of the user to remove. Example: `38689843`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `userId` | number |  |

## Native endpoint

Through the native Mighty Networks API, this operation is `DELETE /networks/:network_id/spaces/:space_id/members/:user_id/` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-space-member.md) for the provider-specific parameters and requirements.

