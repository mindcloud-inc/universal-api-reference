# TxtSync: Preview SMS

Previews an SMS message in TxtSync.

```
GET https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/preview-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/preview-sms?connectionId=$CONNECTION_ID&message=string&index=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "message": "string",
  "index": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/preview-sms?${params}`, {
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
| `to` | string | no |  |
| `toContactIds` | list<number> | no | Accepts multiple values as an array. |
| `toTagIds` | list<number> | no | Accepts multiple values as an array. |
| `message` | string | yes |  |
| `index` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AllowSMS": true,
      "ApproxCostGBP": 1,
      "ApproxCostLocal": 1,
      "ApproxSegmentsPerSms": 1,
      "BalanceGBP": 1,
      "BalanceLocal": 1,
      "Contact": {},
      "ContainsEmojis": true,
      "CurrencyCode": "string",
      "Destinations": [
        {}
      ],
      "FoundContact": true,
      "LinkDetails": [
        {}
      ],
      "Message": "string",
      "TotalSendableContacts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AllowSMS` | boolean |  |
| `ApproxCostGBP` | number |  |
| `ApproxCostLocal` | number |  |
| `ApproxSegmentsPerSms` | number |  |
| `BalanceGBP` | number |  |
| `BalanceLocal` | number |  |
| `Contact` | object |  |
| `ContainsEmojis` | boolean |  |
| `CurrencyCode` | string |  |
| `Destinations` | array<object> |  |
| `FoundContact` | boolean |  |
| `LinkDetails` | array<object> |  |
| `Message` | string |  |
| `TotalSendableContacts` | number |  |

## Native endpoint

Through the native TxtSync API, this operation is `POST /sms/preview` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-sms.md) for the provider-specific parameters and requirements.

