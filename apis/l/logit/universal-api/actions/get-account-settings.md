# Logit: Get Account Settings

Retrieves account settings from Logit.

```
GET https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-account-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-account-settings?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-account-settings?${params}`, {
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
| `accountId` | string | yes | The ID of a Logit account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "displayName": "Ava Chen",
      "force2FA": true,
      "isEnabled": true,
      "isPaying": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `displayName` | string |  |
| `force2FA` | boolean |  |
| `isEnabled` | boolean |  |
| `isPaying` | boolean |  |

## Native endpoint

Through the native Logit API, this operation is `GET /api/account/:accountId/settings` (base URL `https://dashboard.logit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-settings.md) for the provider-specific parameters and requirements.

