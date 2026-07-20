# Snapchat Ads: Get Organization

Retrieves an organization from Snapchat Ads.

```
GET https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/get-organization?${params}`, {
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
| `organizationId` | string | yes | The Snapchat Organization ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organizations": [
        {
          "organization": {
            "created_at": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "name": "Ava Chen"
          }
        }
      ],
      "request_id": "string",
      "request_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organizations[].organization.created_at` | date |  |
| `organizations[].organization.id` | string |  |
| `organizations[].organization.name` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Ads API, this operation is `GET /organizations/:organizationId` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

