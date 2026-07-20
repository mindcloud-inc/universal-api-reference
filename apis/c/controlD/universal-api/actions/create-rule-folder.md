# Control D: Create Rule Folder

Creates a rule folder in Control D.

```
POST https://connect.mindcloud.co/v1/universal/controlD/latest/actions/create-rule-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/create-rule-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileId": "string",
  "name": "Ava Chen",
  "do": 1,
  "status": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/controlD/latest/actions/create-rule-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileId": "string",
    "name": "Ava Chen",
    "do": 1,
    "status": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileId` | string | yes | Primary key (PK) of the profile |
| `name` | string | yes | Name of your folder |
| `do` | number | yes | Add a rule type to a folder. All rules inside will inherit rule type. 0 = BLOCK. 1 = BYPASS, 2 = SPOOF, 3 = REDIRECT |
| `via` | string | no | Add spoof IP or hostname, or proxy identiifer if do=2 or do=3. |
| `status` | number | yes | Status of the folder and all rules inside |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": {},
      "count": 1,
      "group": "string",
      "PK": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | object |  |
| `count` | number |  |
| `group` | string |  |
| `PK` | number |  |

## Native endpoint

Through the native Control D API, this operation is `POST /profiles/:profileId/groups` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-rule-folder.md) for the provider-specific parameters and requirements.

