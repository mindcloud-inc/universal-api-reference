# Dialpad: List Channel Members

Retrieves members of a Dialpad channel.

```
GET https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-channel-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-channel-members?connectionId=$CONNECTION_ID&id=1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-channel-members?${params}`, {
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
| `id` | string | yes | The channel id. Example: `1234567890`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | A token used to return the next page of a previous request. Use the cursor provided in the previous response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Dialpad API, this operation is `GET /channels/:id/members` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-members.md) for the provider-specific parameters and requirements.

