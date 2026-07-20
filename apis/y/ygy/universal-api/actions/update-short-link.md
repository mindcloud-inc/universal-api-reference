# y.gy: Update Short Link

Updates an existing short link in y.gy.

```
PUT https://connect.mindcloud.co/v1/universal/ygy/latest/actions/update-short-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a y.gy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ygy/latest/actions/update-short-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ygy/latest/actions/update-short-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addTags` | list<number> | no |  |
| `androidLinkDestination` | string | no |  |
| `botProtection` | boolean | no |  |
| `captcha` | boolean | no |  |
| `destinationUrl` | string | no |  |
| `expirationDate` | date | no |  |
| `id` | string | yes |  |
| `iosLinkDestination` | string | no |  |
| `name` | string | no |  |
| `ogDescription` | string | no |  |
| `ogImage` | string | no |  |
| `ogTitle` | string | no |  |
| `password` | string | no |  |
| `qrCodeBackgroundHex` | string | no |  |
| `qrCodeForegroundHex` | string | no |  |
| `removeTags` | list<number> | no |  |
| `webhookAuthKey` | string | no |  |
| `webhookUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Android Link Destination": "https://example.com",
      "Bot Protection": true,
      "Captcha": true,
      "Created At": "string",
      "Destination URL": "https://example.com",
      "Domain": "string",
      "Expiration Date": "string",
      "Has Password": true,
      "ID": 1,
      "iOS Link Destination": "https://example.com",
      "Name": "Ava Chen",
      "OG Description": "string",
      "OG Image": "string",
      "OG Title": "string",
      "Organization ID": 1,
      "QR Code Background Hex": "string",
      "QR Code Foreground Hex": "string",
      "QR Code PNG": "string",
      "QR Code SVG": "string",
      "Suffix": "string",
      "Tags": [
        {}
      ],
      "URL": "https://example.com",
      "Webhook URL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Android Link Destination` | string | Android-specific destination URL. |
| `Bot Protection` | boolean | Whether bot protection is enabled. |
| `Captcha` | boolean | Whether captcha is enabled. |
| `Created At` | string | When the link was created. |
| `Destination URL` | string | The link destination URL. |
| `Domain` | string | The short-link domain. |
| `Expiration Date` | string | Optional expiration date. |
| `Has Password` | boolean | Whether the link is password protected. |
| `ID` | number | Unique short link identifier. |
| `iOS Link Destination` | string | iOS-specific destination URL. |
| `Name` | string | Internal link name. |
| `OG Description` | string | Open Graph description. |
| `OG Image` | string | Open Graph image URL. |
| `OG Title` | string | Open Graph title. |
| `Organization ID` | number | Owning organization identifier. |
| `QR Code Background Hex` | string | QR background color. |
| `QR Code Foreground Hex` | string | QR foreground color. |
| `QR Code PNG` | string | PNG QR code URL. |
| `QR Code SVG` | string | SVG QR code markup. |
| `Suffix` | string | The short-link suffix. |
| `Tags` | array<object> | Tags attached to the link. |
| `URL` | string | The generated short URL. |
| `Webhook URL` | string | Webhook destination URL. |

## Native endpoint

Through the native y.gy API, this operation is `PATCH /api/v1/link/:id` (base URL `https://api.y.gy`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-short-link.md) for the provider-specific parameters and requirements.

