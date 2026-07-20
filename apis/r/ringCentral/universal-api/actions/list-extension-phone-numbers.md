# RingCentral: List Extension Phone Numbers

Retrieves phone numbers for a RingCentral extension.

```
GET https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-extension-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RingCentral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-extension-phone-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=string&extensionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "string",
  "extensionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-extension-phone-numbers?${params}`, {
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
| `accountId` | string | yes |  |
| `extensionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callerIdName": "Ava Chen",
      "country": {
        "id": "string",
        "name": "Ava Chen",
        "uri": "string"
      },
      "features": [
        "string"
      ],
      "id": 1,
      "location": "string",
      "paymentType": "string",
      "phoneNumber": "string",
      "primary": true,
      "status": "string",
      "type": "string",
      "uri": "string",
      "usageType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callerIdName` | string |  |
| `country.id` | string |  |
| `country.name` | string |  |
| `country.uri` | string |  |
| `features[]` | string |  |
| `id` | number |  |
| `location` | string |  |
| `paymentType` | string |  |
| `phoneNumber` | string |  |
| `primary` | boolean |  |
| `status` | string |  |
| `type` | string |  |
| `uri` | string |  |
| `usageType` | string |  |

## Native endpoint

Through the native RingCentral API, this operation is `GET restapi/v1.0/account/:accountId/extension/:extensionId/phone-number` (base URL `https://platform.ringcentral.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-extension-phone-numbers.md) for the provider-specific parameters and requirements.

