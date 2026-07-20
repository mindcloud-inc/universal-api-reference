# Routee: Retrieve information for a specific email address from a specific campaign

Retrieves information for a specific email address from a specific campaign in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-information-for-a-specific-email-address-from-a-specific-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-information-for-a-specific-email-address-from-a-specific-campaign?connectionId=$CONNECTION_ID&id=string&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-information-for-a-specific-email-address-from-a-specific-campaign?${params}`, {
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
| `id` | string | yes | Campaign id |
| `email` | string | yes | Email address to retrieve the information |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detail_status": 1,
      "detail_status_explain": "string",
      "global_status": 1,
      "global_status_explain": "string",
      "sent_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detail_status` | number |  |
| `detail_status_explain` | string |  |
| `global_status` | number |  |
| `global_status_explain` | string |  |
| `sent_date` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /campaigns/:id/email/:email` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-information-for-a-specific-email-address-from-a-specific-campaign.md) for the provider-specific parameters and requirements.

