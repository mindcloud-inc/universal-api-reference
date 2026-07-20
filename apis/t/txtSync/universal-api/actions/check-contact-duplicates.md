# TxtSync: Check Contact Duplicates

Retrieves duplicate contact matches from TxtSync.

```
GET https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/check-contact-duplicates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/check-contact-duplicates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/check-contact-duplicates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "Contacts": [
        {}
      ],
      "MobileNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Contacts` | array<object> |  |
| `MobileNumber` | string |  |

## Native endpoint

Through the native TxtSync API, this operation is `GET /contacts/duplicates` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-contact-duplicates.md) for the provider-specific parameters and requirements.

