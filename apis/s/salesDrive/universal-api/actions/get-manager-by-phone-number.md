# SalesDrive: Get Manager By Phone Number

Retrieves manager and contact details by phone number in SalesDrive.

```
GET https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/get-manager-by-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/get-manager-by-phone-number?connectionId=$CONNECTION_ID&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/get-manager-by-phone-number?${params}`, {
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
| `phone` | string | yes | Phone number to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {},
      "manager": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `manager` | object |  |
| `status` | string |  |

## Native endpoint

Through the native SalesDrive API, this operation is `GET /api/get_manager_by_phone_number/` (base URL `https://{{credentials.account}}.salesdrive.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-manager-by-phone-number.md) for the provider-specific parameters and requirements.

