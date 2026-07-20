# CampaignKit: Validate Emails

Validates one or more email addresses in CampaignKit.

```
GET https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/validate-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CampaignKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/validate-emails?connectionId=$CONNECTION_ID&emails%5B%5D=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emails[]": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/validate-emails?${params}`, {
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
| `emails[]` | array<string> | yes | One to one hundred email addresses to validate in a single request. |

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
| `results[].contextId` | string |  |
| `results[].email` | string |  |
| `results[].result.classifier` | string |  |
| `results[].result.description[]` | array<string> |  |
| `results[].result.mailbox` | string |  |
| `results[].result.mx` | string |  |
| `results[].result.score` | number |  |
| `results[].result.smtpResponse` | string |  |
| `results[].result.syntax` | string |  |

## Native endpoint

Through the native CampaignKit API, this operation is `POST /v1/email/validate` (base URL `https://api.campaignkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-emails.md) for the provider-specific parameters and requirements.

