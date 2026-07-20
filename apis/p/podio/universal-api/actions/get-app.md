# Podio: Get App

Retrieves an existing app from Podio.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-app?connectionId=$CONNECTION_ID&appId=123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-app?${params}`, {
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
| `appId` | number | yes | The app ID. Example: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": 1,
      "config": {},
      "currentRevision": 1,
      "defaultViewId": 1,
      "fields": [
        {}
      ],
      "integration": {},
      "isDefault": true,
      "itemAccountingInfo": {},
      "layouts": {},
      "link": "https://example.com",
      "linkAdd": "https://example.com",
      "mailbox": "string",
      "original": 1,
      "originalRevision": 1,
      "owner": {},
      "rights": [
        "string"
      ],
      "sharefileVaultUrl": "https://example.com",
      "spaceId": 1,
      "status": "string",
      "subscribed": true,
      "token": "string",
      "url": "https://example.com",
      "urlAdd": "https://example.com",
      "urlLabel": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | number |  |
| `config` | object |  |
| `currentRevision` | number |  |
| `defaultViewId` | number |  |
| `fields` | array<object> |  |
| `integration` | object |  |
| `isDefault` | boolean |  |
| `itemAccountingInfo` | object |  |
| `layouts` | object |  |
| `link` | string |  |
| `linkAdd` | string |  |
| `mailbox` | string |  |
| `original` | number |  |
| `originalRevision` | number |  |
| `owner` | object |  |
| `rights` | array<string> |  |
| `sharefileVaultUrl` | string |  |
| `spaceId` | number |  |
| `status` | string |  |
| `subscribed` | boolean |  |
| `token` | string |  |
| `url` | string |  |
| `urlAdd` | string |  |
| `urlLabel` | string |  |

## Native endpoint

Through the native Podio API, this operation is `GET /app/:app_id` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app.md) for the provider-specific parameters and requirements.

