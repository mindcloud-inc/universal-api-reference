# Go4Clients: Get Email Campaign

Retrieves an email campaign from Go4Clients.

```
GET https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-email-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-email-campaign?connectionId=$CONNECTION_ID&campaignId=69dd2653841fc80008eba9e1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "69dd2653841fc80008eba9e1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-email-campaign?${params}`, {
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
| `campaignId` | string | yes | Email campaign identifier. Example: `69dd2653841fc80008eba9e1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "starDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string | Email body content. |
| `creationDate` | date | Campaign creation date. |
| `id` | string | Identifier of the email campaign. |
| `name` | string | Name of the email campaign. |
| `starDate` | date | Campaign start date. |

## Native endpoint

Through the native Go4Clients API, this operation is `GET /api/campaigns/email/v1.0/{{campaignId}}` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-campaign.md) for the provider-specific parameters and requirements.

