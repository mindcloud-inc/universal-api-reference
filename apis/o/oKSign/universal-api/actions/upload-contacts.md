# OKSign: Upload Contacts

Creates or updates contacts in OKSign.

```
POST https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/upload-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OKSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/upload-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/upload-contacts', {
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
      "reason": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reason` | string | Contacts upload result payload. |
| `status` | string |  |

## Native endpoint

Through the native OKSign API, this operation is `POST /contacts/upload` (base URL `https://www.oksign.be/services/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-contacts.md) for the provider-specific parameters and requirements.

