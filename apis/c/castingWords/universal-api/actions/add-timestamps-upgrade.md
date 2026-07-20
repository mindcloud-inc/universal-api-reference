# CastingWords: Add Timestamps Upgrade

Updates a CastingWords order to add timestamps.

```
PUT https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/add-timestamps-upgrade
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CastingWords `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/add-timestamps-upgrade" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audiofile_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/add-timestamps-upgrade', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audiofile_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audiofile_id` | string | yes | CastingWords audiofile ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `test` | string | no | Set to 1 to run a CastingWords test upgrade. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | CastingWords result message. |

## Native endpoint

Through the native CastingWords API, this operation is `POST audiofile/:audiofile_id/upgrade` (base URL `https://castingwords.com/store/API4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-timestamps-upgrade.md) for the provider-specific parameters and requirements.

