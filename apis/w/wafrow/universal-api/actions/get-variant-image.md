# Wafrow: Get Variant Image

Retrieves a rendered variant image from Wafrow.

```
GET https://connect.mindcloud.co/v1/universal/wafrow/latest/actions/get-variant-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wafrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wafrow/latest/actions/get-variant-image?connectionId=$CONNECTION_ID&templateId=string&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string",
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wafrow/latest/actions/get-variant-image?${params}`, {
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
| `templateId` | string | yes | The Wafrow template UUID to render from the saved variant. |
| `campaignId` | string | yes | The saved Wafrow campaign preset UUID returned by Save Variant. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wafrow API returns.

## Native endpoint

Through the native Wafrow API, this operation is `GET /i/:template_id/:campaign_id` (base URL `https://wafrow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variant-image.md) for the provider-specific parameters and requirements.

