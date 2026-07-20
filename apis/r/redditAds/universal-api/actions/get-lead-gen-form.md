# Reddit Lead Ads: Get Lead Gen Form

Retrieves a lead generation form from Reddit Ads.

```
GET https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-lead-gen-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Lead Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-lead-gen-form?connectionId=$CONNECTION_ID&leadGenFormId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadGenFormId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-lead-gen-form?${params}`, {
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
| `leadGenFormId` | string | yes | Reddit Ads lead generation form identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `id` | string | Lead generation form identifier. |
| `name` | string | Lead generation form name. |

## Native endpoint

Through the native Reddit Lead Ads API, this operation is `GET /lead_gen_forms/{lead_gen_form_id}` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-gen-form.md) for the provider-specific parameters and requirements.

