# UpGuard: Get Vendor Questionnaire Metadata

Retrieves metadata for a vendor questionnaire in UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-vendor-questionnaire-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-vendor-questionnaire-metadata?connectionId=$CONNECTION_ID&questionnaireId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionnaireId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-vendor-questionnaire-metadata?${params}`, {
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
| `questionnaireId` | number | yes | The numeric ID of the questionnaire to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UpGuard API returns.

## Native endpoint

Through the native UpGuard API, this operation is `GET /vendor/questionnaire` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor-questionnaire-metadata.md) for the provider-specific parameters and requirements.

