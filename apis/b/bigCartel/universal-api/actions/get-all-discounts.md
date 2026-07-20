# Big Cartel: Get All Discounts

Retrieves discounts from Big Cartel.

```
GET https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-all-discounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Big Cartel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-all-discounts?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-all-discounts?${params}`, {
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
| `accountId` | number | yes | The Big Cartel account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "activeAt": "string",
        "applicationType": "string",
        "code": "string",
        "expirationType": "string",
        "expiresAt": "string",
        "includesFreeShipping": true,
        "name": "Ava Chen",
        "percentDiscount": 1,
        "requirementType": "string",
        "rewardType": "string",
        "useCount": 1
      },
      "id": "string",
      "meta": {
        "count": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.activeAt` | string |  |
| `attributes.applicationType` | string |  |
| `attributes.code` | string |  |
| `attributes.expirationType` | string |  |
| `attributes.expiresAt` | string |  |
| `attributes.includesFreeShipping` | boolean |  |
| `attributes.name` | string |  |
| `attributes.percentDiscount` | number |  |
| `attributes.requirementType` | string |  |
| `attributes.rewardType` | string |  |
| `attributes.useCount` | number |  |
| `id` | string |  |
| `meta.count` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Big Cartel API, this operation is `GET /v1/accounts/[:account-id]/discounts` (base URL `https://api.bigcartel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-discounts.md) for the provider-specific parameters and requirements.

