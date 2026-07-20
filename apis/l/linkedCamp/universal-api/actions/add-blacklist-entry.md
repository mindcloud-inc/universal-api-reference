# LinkedCamp: Add Blacklist Entry



```
POST https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/add-blacklist-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedCamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/add-blacklist-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keyword": "string",
  "type": "string",
  "linkedInAccountEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/add-blacklist-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keyword": "string",
    "type": "string",
    "linkedInAccountEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `keyword` | string | yes | Blacklist keyword or value. |
| `type` | string | yes | Blacklist type: PROFILE_URL, KEYWORD, or JOB_TITLE. |
| `linkedInAccountEmail` | string | yes | LinkedIn account email for the blacklist entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | LinkedCamp status message. |
| `success` | boolean | Whether the operation succeeded. |

## Native endpoint

Through the native LinkedCamp API, this operation is `POST /blacklists` (base URL `https://api.linkedcamp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-blacklist-entry.md) for the provider-specific parameters and requirements.

