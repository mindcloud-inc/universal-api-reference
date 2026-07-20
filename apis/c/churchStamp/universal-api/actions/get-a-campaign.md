# ChurchStamp: Get a Campaign

Retrieves campaign details from ChurchStamp by campaign ID.

```
GET https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/get-a-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChurchStamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/get-a-campaign?connectionId=$CONNECTION_ID&campaignId=1731535111267x707091876624990200" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1731535111267x707091876624990200"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/get-a-campaign?${params}`, {
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
| `campaignId` | string | yes | Unique identifier for the campaign. Example: `1731535111267x707091876624990200`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "Address": "string",
      "Design_id": "string",
      "Name": "Ava Chen",
      "Return URL": "https://example.com",
      "User": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `Address` | string |  |
| `Design_id` | string |  |
| `Name` | string |  |
| `Return URL` | string |  |
| `User` | string |  |

## Native endpoint

Through the native ChurchStamp API, this operation is `GET /get-a-campaigns` (base URL `https://v2.churchstamp.com/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-campaign.md) for the provider-specific parameters and requirements.

