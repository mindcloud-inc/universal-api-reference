# Checkmk: Acknowledge Host Problems

Creates host problem acknowledgements in Checkmk.

```
POST https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/acknowledge-host-problems
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkmk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/acknowledge-host-problems" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hostName": "Ava Chen",
  "comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/acknowledge-host-problems', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hostName": "Ava Chen",
    "comment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hostName` | string | yes | Host whose problems should be acknowledged. |
| `comment` | string | yes | Acknowledgement comment. |
| `sticky` | boolean | no | Whether acknowledgements should be sticky. Default: `true`. |
| `persistent` | boolean | no | Whether acknowledgements should persist. Default: `false`. |
| `notify` | boolean | no | Whether Checkmk should notify contacts. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extensions": {},
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extensions` | object |  |
| `id` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Checkmk API, this operation is `POST /domain-types/acknowledge/collections/host` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/acknowledge-host-problems.md) for the provider-specific parameters and requirements.

