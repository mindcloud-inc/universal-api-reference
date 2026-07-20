# ChurchStamp: Get Designs

Retrieves a collection of designs from ChurchStamp.

```
GET https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/get-designs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChurchStamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/get-designs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/get-designs?${params}`, {
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
      "_id": "string",
      "Approved": true,
      "Image_Generated": true,
      "mail_id": "string",
      "Name": "Ava Chen",
      "Pdf_Generated": true,
      "Size": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `Approved` | boolean |  |
| `Image_Generated` | boolean |  |
| `mail_id` | string |  |
| `Name` | string |  |
| `Pdf_Generated` | boolean |  |
| `Size` | string |  |

## Native endpoint

Through the native ChurchStamp API, this operation is `GET /get-designs` (base URL `https://v2.churchstamp.com/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-designs.md) for the provider-specific parameters and requirements.

