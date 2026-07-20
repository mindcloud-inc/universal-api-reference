# Dialpad: Create Channel

Creates a new channel in Dialpad.

```
POST https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Test Channel",
  "description": "Temporary test channel for MindCloud verification",
  "privacyType": "private"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Test Channel",
    "description": "Temporary test channel for MindCloud verification",
    "privacyType": "private"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | [single-line only] The name of the channel. Example: `MindCloud Test Channel`. |
| `description` | string | yes | The description of the channel. Example: `Temporary test channel for MindCloud verification`. |
| `privacyType` | list<string> | yes | The privacy type of the channel. One of: `private`, `public`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | no | The ID of the user who owns the channel. Just for company level API key. Example: `6236728822472704`. |

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

Through the native Dialpad API, this operation is `POST /channels` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-channel.md) for the provider-specific parameters and requirements.

