# Atriomail: Get Forwarder



```
GET https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/get-forwarder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atriomail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/get-forwarder?connectionId=$CONNECTION_ID&forwarderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "forwarderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/get-forwarder?${params}`, {
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
| `forwarderId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "address": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "domainId": 1,
      "goto": "string",
      "gotoArray": [
        "string"
      ],
      "id": 1,
      "isCatchAll": true,
      "mailcowId": 1,
      "privateComment": "string",
      "publicComment": "string",
      "syncedAt": "2026-05-07T12:00:00.000Z",
      "syncStatus": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `address` | string |  |
| `createdAt` | date |  |
| `createdBy` | number |  |
| `domainId` | number |  |
| `goto` | string |  |
| `gotoArray` | array<string> |  |
| `id` | number |  |
| `isCatchAll` | boolean |  |
| `mailcowId` | number |  |
| `privateComment` | string |  |
| `publicComment` | string |  |
| `syncedAt` | date |  |
| `syncStatus` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Atriomail API, this operation is `GET /forwarders/:forwarderId` (base URL `https://system.atriomail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-forwarder.md) for the provider-specific parameters and requirements.

