# E2B: Create Sandbox Snapshot

Creates a snapshot from a sandbox in E2B.

```
POST https://connect.mindcloud.co/v1/universal/e2B/latest/actions/create-sandbox-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/create-sandbox-snapshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sandboxId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e2B/latest/actions/create-sandbox-snapshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sandboxId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sandboxId` | string | yes | Identifier of the sandbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "names": [
        "Ava Chen"
      ],
      "snapshotID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `names` | array<string> | Full names of the snapshot template. |
| `snapshotID` | string | Identifier of the snapshot template including tag. |

## Native endpoint

Through the native E2B API, this operation is `POST /sandboxes/{sandboxID}/snapshots` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sandbox-snapshot.md) for the provider-specific parameters and requirements.

