# Maildrip: Retrieve deleted emails of a campaign



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/retrieve-deleted-emails-of-a-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/retrieve-deleted-emails-of-a-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/retrieve-deleted-emails-of-a-campaign?${params}`, {
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
| `campaignId` | string | yes | ID of the campaign to retrieve deleted emails from |
| `limit` | number | no | Number of items per page, use "all" for all items |
| `page` | number | no | Page number for pagination |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedEmails": [
        {}
      ],
      "length": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedEmails` | array<object> |  |
| `length` | number | Number of deleted emails returned |
| `totalPages` | number | Total number of pages |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/campaigns/{campaign_id}/deleted-mails` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-deleted-emails-of-a-campaign.md) for the provider-specific parameters and requirements.

