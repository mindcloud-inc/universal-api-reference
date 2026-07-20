# GAN.AI: Submit Consent

Submits a consent video to GAN.AI.

```
POST https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/submit-consent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/submit-consent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "avatarId": "string",
  "consentVideo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/submit-consent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "avatarId": "string",
    "consentVideo": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `avatarId` | string | yes |  |
| `consentVideo` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GAN.AI API returns.

## Native endpoint

Through the native GAN.AI API, this operation is `POST /v1/consents/submit_consent` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-consent.md) for the provider-specific parameters and requirements.

