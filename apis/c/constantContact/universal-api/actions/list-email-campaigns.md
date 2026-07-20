# Constant Contact: List Email Campaigns

Retrieves email campaigns from Constant Contact.

```
GET https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-email-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-email-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-email-campaigns?${params}`, {
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
| `beforeDate` | date | no | Return campaigns updated before this ISO-8601 datetime. Example: `2026-01-10T11:42:57.000Z`. |
| `afterDate` | date | no | Return campaigns updated after this ISO-8601 datetime. Example: `2026-03-10T11:42:57.000Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaigns": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaigns` | array<object> | Collection of email campaigns. |

## Native endpoint

Through the native Constant Contact API, this operation is `GET /emails` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-campaigns.md) for the provider-specific parameters and requirements.

