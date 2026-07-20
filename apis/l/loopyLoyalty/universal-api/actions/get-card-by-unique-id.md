# Loopy Loyalty: Get Card By Unique ID



```
GET https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-card-by-unique-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-card-by-unique-id?connectionId=$CONNECTION_ID&campaignId=5fcDywPejwj9QszwngBTKg&uniqueIdType=email&uniqueIdValue=taylor.stage3.1774385507840%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "5fcDywPejwj9QszwngBTKg",
  "uniqueIdType": "email",
  "uniqueIdValue": "taylor.stage3.1774385507840@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-card-by-unique-id?${params}`, {
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
| `campaignId` | string | yes | Campaign ID the card belongs to. Example: `5fcDywPejwj9QszwngBTKg`. |
| `uniqueIdType` | string | yes | Unique ID type: email, phone, or text. Example: `email`. |
| `uniqueIdValue` | string | yes | Value for the chosen unique ID type. Example: `taylor.stage3.1774385507840@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card": {
        "campaignId": "string",
        "createTime": "string",
        "customerDetails": {
          "Email Address": "ava@example.com",
          "First Name": "Ava Chen",
          "Mobile Number": "string"
        },
        "id": "string",
        "passStatus": "string",
        "totalRewardsEarned": 1,
        "totalRewardsRedeemed": 1,
        "totalStampsEarned": 1,
        "updateTime": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card.campaignId` | string | Campaign ID the card belongs to. |
| `card.createTime` | string | Card created timestamp. |
| `card.customerDetails.Email Address` | string | Customer email address. |
| `card.customerDetails.First Name` | string | Customer first name. |
| `card.customerDetails.Mobile Number` | string | Customer mobile number. |
| `card.id` | string | Card ID. |
| `card.passStatus` | string | Current pass status. |
| `card.totalRewardsEarned` | number | Lifetime rewards earned. |
| `card.totalRewardsRedeemed` | number | Lifetime rewards redeemed. |
| `card.totalStampsEarned` | number | Lifetime stamps earned. |
| `card.updateTime` | string | Card updated timestamp. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `GET /uniquecard/campaignid/:campaignId/:uniqueIdType/:uniqueIdValue` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card-by-unique-id.md) for the provider-specific parameters and requirements.

