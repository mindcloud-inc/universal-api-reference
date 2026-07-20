# Zoho Campaigns: List Contact Fields

Retrieves all contact fields from Zoho Campaigns.

```
GET https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-contact-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-contact-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-contact-fields?${params}`, {
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
      "blockLabel": "string",
      "blockSequence": 1,
      "displayName": "Ava Chen",
      "fieldDisplayName": "Ava Chen",
      "fieldId": 1,
      "fieldName": "Ava Chen",
      "isMandatory": true,
      "isOtheruserField": true,
      "maxlength": 1,
      "no": 1,
      "sequence": 1,
      "type": "string",
      "uitype": "string",
      "values": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockLabel` | string |  |
| `blockSequence` | number |  |
| `displayName` | string |  |
| `fieldDisplayName` | string |  |
| `fieldId` | number |  |
| `fieldName` | string |  |
| `isMandatory` | boolean |  |
| `isOtheruserField` | boolean |  |
| `maxlength` | number |  |
| `no` | number |  |
| `sequence` | number |  |
| `type` | string |  |
| `uitype` | string |  |
| `values` | string |  |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `GET /contact/allfields` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-fields.md) for the provider-specific parameters and requirements.

