# Vero: Retrieve Campaign

Retrieves a campaign record from Vero.

```
GET https://connect.mindcloud.co/v1/universal/vero/latest/actions/retrieve-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vero/latest/actions/retrieve-campaign?connectionId=$CONNECTION_ID&id=campaign_example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "campaign_example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vero/latest/actions/retrieve-campaign?${params}`, {
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
| `id` | string | yes | The campaign identifier. Default: `campaign_example`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Campaign identifier. |
| `object` | string | Resource type. |
| `status` | string | Campaign status. |
| `title` | string | Campaign title. |

## Native endpoint

Through the native Vero API, this operation is `GET /api/v4/campaigns/:id` (base URL `https://api.getvero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-campaign.md) for the provider-specific parameters and requirements.

