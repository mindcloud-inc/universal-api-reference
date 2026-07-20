# Kiwili: Get Company Details

Retrieves details for a company in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-company-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-company-details?connectionId=$CONNECTION_ID&company_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-company-details?${params}`, {
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
| `company_id` | string | yes | The Kiwili company ID. Use the string 0 for the active company profile. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AddressList": [
        {}
      ],
      "AdministrativeNumber": "string",
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AddressList` | array<object> |  |
| `AdministrativeNumber` | string |  |
| `Name` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /company/:company_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-details.md) for the provider-specific parameters and requirements.

