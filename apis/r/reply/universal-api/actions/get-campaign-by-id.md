# Reply: Get Campaign By Id



```
GET https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-campaign-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-campaign-by-id?connectionId=$CONNECTION_ID&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-campaign-by-id?${params}`, {
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
| `campaignId` | number | yes | Reply campaign identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bouncesCount": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "deliveriesCount": 1,
      "emailAccount": "ava@example.com",
      "emailAccounts": [
        "ava@example.com"
      ],
      "id": 1,
      "name": "Ava Chen",
      "opensCount": 1,
      "optOutsCount": 1,
      "outOfOfficeCount": 1,
      "ownerEmail": "ava@example.com",
      "peopleActive": 1,
      "peopleCount": 1,
      "peopleFinished": 1,
      "peoplePaused": 1,
      "repliesCount": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bouncesCount` | number | Total bounces for the campaign. |
| `created` | date | Timestamp when the campaign was created. |
| `deliveriesCount` | number | Total deliveries for the campaign. |
| `emailAccount` | string | Primary sending email account when present. |
| `emailAccounts` | array<string> | Sending email accounts associated with the campaign. |
| `id` | number | Reply campaign identifier. |
| `name` | string | Campaign name. |
| `opensCount` | number | Total opens for the campaign. |
| `optOutsCount` | number | Total opt-outs for the campaign. |
| `outOfOfficeCount` | number | Total out-of-office replies for the campaign. |
| `ownerEmail` | string | Campaign owner email address. |
| `peopleActive` | number | Contacts currently active in the campaign. |
| `peopleCount` | number | Total contacts in the campaign. |
| `peopleFinished` | number | Contacts that finished the campaign. |
| `peoplePaused` | number | Contacts currently paused in the campaign. |
| `repliesCount` | number | Total replies for the campaign. |
| `status` | number | Campaign status code. |

## Native endpoint

Through the native Reply API, this operation is `GET /v1/campaigns` (base URL `https://api.reply.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-by-id.md) for the provider-specific parameters and requirements.

