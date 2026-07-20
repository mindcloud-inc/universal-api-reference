# Lasso X: Lookup Phone Number

Finds a phone number in Lasso X by number.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/lookup-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/lookup-phone-number?connectionId=$CONNECTION_ID&phone_number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone_number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/lookup-phone-number?${params}`, {
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
| `phone_number` | string | yes | Phone number to look up. |
| `include_company` | boolean | no | Whether to include company details in the phone lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "added": "2026-05-07T12:00:00.000Z",
          "address1": "string",
          "city": "string",
          "company": {
            "companyType": "string",
            "employeeCount": 1,
            "localIdentifier": "string",
            "places": [
              {
                "lassoId": "string"
              }
            ],
            "primaryIndustry": "string",
            "statusCode": "string"
          },
          "cvr": 1,
          "lassoId": "string",
          "organizationName": "Ava Chen",
          "personFirstName": "Ava",
          "personLastName": "Chen",
          "postalCode": 1,
          "supplier": "string",
          "telephoneNumber": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].added` | date |  |
| `[].address1` | string |  |
| `[].city` | string |  |
| `[].company.companyType` | string |  |
| `[].company.employeeCount` | number |  |
| `[].company.localIdentifier` | string |  |
| `[].company.places[].lassoId` | string |  |
| `[].company.primaryIndustry` | string |  |
| `[].company.statusCode` | string |  |
| `[].cvr` | number |  |
| `[].lassoId` | string |  |
| `[].organizationName` | string |  |
| `[].personFirstName` | string |  |
| `[].personLastName` | string |  |
| `[].postalCode` | number |  |
| `[].supplier` | string |  |
| `[].telephoneNumber` | number |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /data/teledata/:phoneNumber` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-phone-number.md) for the provider-specific parameters and requirements.

