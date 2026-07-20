# Constant Contact: Delete Email Campaign

Deletes an email campaign from Constant Contact.

```
DELETE https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/delete-email-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/delete-email-campaign?connectionId=$CONNECTION_ID&campaignId=91569d46-00e4-4a4d-9a4c-d17d98740d04" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "91569d46-00e4-4a4d-9a4c-d17d98740d04"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/delete-email-campaign?${params}`, {
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
| `campaignId` | string | yes | The unique identifier for the email campaign to delete. Example: `91569d46-00e4-4a4d-9a4c-d17d98740d04`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string |  |

## Native endpoint

Through the native Constant Contact API, this operation is `DELETE /emails/:campaign_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-email-campaign.md) for the provider-specific parameters and requirements.

