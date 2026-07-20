# CreateSend: Get Campaign Summary

Retrieves a campaign summary from CreateSend.

```
GET https://connect.mindcloud.co/v1/universal/createSend/latest/actions/get-campaign-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CreateSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/createSend/latest/actions/get-campaign-summary?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/createSend/latest/actions/get-campaign-summary?${params}`, {
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
| `campaignId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Recipients": 1,
      "TotalOpened": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Recipients` | number | Number of campaign recipients. |
| `TotalOpened` | number | Number of opens recorded. |

## Native endpoint

Through the native CreateSend API, this operation is `GET /campaigns/:campaignId/summary.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-summary.md) for the provider-specific parameters and requirements.

