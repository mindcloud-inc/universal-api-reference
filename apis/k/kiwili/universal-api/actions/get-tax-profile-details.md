# Kiwili: Get Tax Profile Details

Retrieves details for a tax profile in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-tax-profile-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-tax-profile-details?connectionId=$CONNECTION_ID&tax_profile_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tax_profile_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-tax-profile-details?${params}`, {
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
| `tax_profile_id` | string | yes | The Kiwili tax profile ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Description": "string",
      "Id": 1,
      "IsActive": true,
      "IsDefaultTax": true,
      "IsGrossTax2": true,
      "Tax1": 1,
      "Tax1Label": "string",
      "Tax1Number": "string",
      "Tax2": 1,
      "Tax2Label": "string",
      "Tax2Number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Description` | string |  |
| `Id` | number |  |
| `IsActive` | boolean |  |
| `IsDefaultTax` | boolean |  |
| `IsGrossTax2` | boolean |  |
| `Tax1` | number |  |
| `Tax1Label` | string |  |
| `Tax1Number` | string |  |
| `Tax2` | number |  |
| `Tax2Label` | string |  |
| `Tax2Number` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /taxprofile/:tax_profile_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tax-profile-details.md) for the provider-specific parameters and requirements.

