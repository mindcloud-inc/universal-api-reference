# Zoho Campaigns: List Segment Contacts

Retrieves contacts from a Zoho Campaigns segment.

```
GET https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-segment-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-segment-contacts?connectionId=$CONNECTION_ID&cvid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cvid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-segment-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cvid` | string | yes | Segment ID (`cvid`) to read contacts from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedTime": "string",
      "companyname": "Ava Chen",
      "contactEmail": "ava@example.com",
      "firstname": "Ava",
      "lastname": "Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedTime` | string | When the contact was added to the segment. |
| `companyname` | string | Segment contact company name. |
| `contactEmail` | string | Segment contact email address. |
| `firstname` | string | Segment contact first name. |
| `lastname` | string | Segment contact last name. |
| `phone` | string | Segment contact phone number. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `GET /getsegmentcontacts` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segment-contacts.md) for the provider-specific parameters and requirements.

