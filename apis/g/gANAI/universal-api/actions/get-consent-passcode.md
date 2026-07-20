# GAN.AI: Get Consent Passcode

Retrieves a passcode for a GAN.AI consent video.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-consent-passcode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-consent-passcode?connectionId=$CONNECTION_ID&avatarId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "avatarId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-consent-passcode?${params}`, {
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
| `avatarId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expireAt": 1,
      "passcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expireAt` | number | Passcode expiration time. |
| `passcode` | string | Passcode to use in the consent video. |

## Native endpoint

Through the native GAN.AI API, this operation is `GET /v1/consents/consent_passcode` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-consent-passcode.md) for the provider-specific parameters and requirements.

