# NobelSMS: Create Blacklist Entry

Creates a new blacklist entry in NobelSMS.

```
POST https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/create-blacklist-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NobelSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/create-blacklist-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bnumber": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/create-blacklist-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bnumber": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bnumber` | number | yes | B-number. |
| `tagId` | number | no | Tag ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native NobelSMS API, this operation is `POST /black_list` (base URL `https://api.nobelsms.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-blacklist-entry.md) for the provider-specific parameters and requirements.

