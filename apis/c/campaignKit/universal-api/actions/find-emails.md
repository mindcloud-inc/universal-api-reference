# CampaignKit: Find Emails

Finds professional email addresses in CampaignKit by name and domain.

```
GET https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/find-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CampaignKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/find-emails?connectionId=$CONNECTION_ID&entries%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entries[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/find-emails?${params}`, {
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
| `entries[]` | array<object> | yes | Up to 20 entries with name or firstName/lastName plus domain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "results": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `results[]` | array<object> |  |
| `results[].domain` | string |  |
| `results[].email` | string |  |
| `results[].found` | boolean |  |
| `results[].name` | string |  |

## Native endpoint

Through the native CampaignKit API, this operation is `POST /v1/email/find` (base URL `https://api.campaignkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-emails.md) for the provider-specific parameters and requirements.

