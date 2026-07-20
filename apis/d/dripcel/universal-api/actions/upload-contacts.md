# Dripcel: Upload Contacts

Creates new contacts in Dripcel.

```
POST https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/upload-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dripcel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/upload-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/upload-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "validContact": 1
      },
      "ok": true,
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.validContact` | number |  |
| `ok` | boolean |  |
| `requestId` | string |  |

## Native endpoint

Through the native Dripcel API, this operation is `POST /contacts` (base URL `https://api.dripcel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-contacts.md) for the provider-specific parameters and requirements.

