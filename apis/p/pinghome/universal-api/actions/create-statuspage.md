# Pinghome: Create Statuspage

Creates a new statuspage in Pinghome.

```
POST https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-statuspage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-statuspage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Status",
  "description": "MindCloud public status page",
  "subdomain": "mindcloud-20260330-1749",
  "type": "public",
  "components": [],
  "groups": []
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-statuspage', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Status",
    "description": "MindCloud public status page",
    "subdomain": "mindcloud-20260330-1749",
    "type": "public",
    "components": [],
    "groups": []
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Statuspage name. Example: `MindCloud Status`. |
| `description` | string | yes | Statuspage description. Example: `MindCloud public status page`. |
| `subdomain` | string | yes | Statuspage subdomain. Example: `mindcloud-20260330-1749`. |
| `type` | string | yes | Statuspage type. Example: `public`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `components` | string | yes | JSON array of components. Default: `[]`. |
| `groups` | string | yes | JSON array of groups. Default: `[]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "statuspage": {
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `statuspage.id` | string | Statuspage ID |

## Native endpoint

Through the native Pinghome API, this operation is `POST /statuspage-cmd/v1/statuspage` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-statuspage.md) for the provider-specific parameters and requirements.

