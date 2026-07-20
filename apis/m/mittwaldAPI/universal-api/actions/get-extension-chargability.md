# mittwald: Get Extension Chargability

Retrieves whether an extension is chargeable from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-extension-chargability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-extension-chargability?connectionId=$CONNECTION_ID&contextId=string&extensionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contextId": "string",
  "extensionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-extension-chargability?${params}`, {
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
| `contextId` | string | yes | The unique identifier of the extension context. |
| `extensionId` | string | yes | The unique identifier of the extension. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chargeability": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chargeability` | string |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/extensions/:extensionId/contexts/:contextId/chargability` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extension-chargability.md) for the provider-specific parameters and requirements.

