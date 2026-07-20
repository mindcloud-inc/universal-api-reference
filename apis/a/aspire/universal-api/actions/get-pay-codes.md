# Aspire: Get Pay Codes

Retrieves pay codes from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-pay-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-pay-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-pay-codes?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderby` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "excludeFromOT": true,
      "fixedRate": {},
      "oTPaycode": true,
      "payCode": "string",
      "payCodeID": 1,
      "payCodeName": "Ava Chen",
      "payCodeType": "string",
      "premiumDollars": {},
      "premiumPercent": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `excludeFromOT` | boolean |  |
| `fixedRate` | object |  |
| `oTPaycode` | boolean |  |
| `payCode` | string |  |
| `payCodeID` | number |  |
| `payCodeName` | string |  |
| `payCodeType` | string |  |
| `premiumDollars` | object |  |
| `premiumPercent` | object |  |

## Native endpoint

Through the native Aspire API, this operation is `GET PayCodes` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pay-codes.md) for the provider-specific parameters and requirements.

