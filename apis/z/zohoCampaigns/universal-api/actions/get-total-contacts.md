# Zoho Campaigns: Get Total Contacts

Retrieves total contacts from a Zoho Campaigns list.

```
GET https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/get-total-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/get-total-contacts?connectionId=$CONNECTION_ID&listKey=34715a953809d0b01f02e6548dcf32a2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listKey": "34715a953809d0b01f02e6548dcf32a2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/get-total-contacts?${params}`, {
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
| `listKey` | string | yes | Mailing list key to count subscribers for. Example: `34715a953809d0b01f02e6548dcf32a2`. |
| `status` | string | no | Subscriber status to count. One of: `0`, `1`, `2`, `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "noOfContacts": 1,
      "status": "string",
      "uri": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Provider response code. |
| `noOfContacts` | number | Total number of contacts in the mailing list. |
| `status` | string | Provider status for the request. |
| `uri` | string | Provider endpoint identifier. |
| `version` | string | Provider API version. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `GET /listsubscriberscount` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-total-contacts.md) for the provider-specific parameters and requirements.

