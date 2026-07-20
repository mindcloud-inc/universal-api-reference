# RotaCloud: Update User Onboarding



```
PUT https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-user-onboarding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-user-onboarding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "title": "string",
  "gender": "string",
  "dob": "string",
  "address1": "string",
  "address2": "string",
  "county": "string",
  "phone": "string",
  "postcode": "string",
  "city": "string",
  "emergencyContactName": "Ava Chen",
  "emergencyContactPhone": "string",
  "emergencyContactRelationship": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-user-onboarding', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "title": "string",
    "gender": "string",
    "dob": "string",
    "address1": "string",
    "address2": "string",
    "county": "string",
    "phone": "string",
    "postcode": "string",
    "city": "string",
    "emergencyContactName": "Ava Chen",
    "emergencyContactPhone": "string",
    "emergencyContactRelationship": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Onboarding user ID. |
| `title` | string | yes | User title. |
| `gender` | string | yes | User gender. |
| `dob` | string | yes | Date of birth in YYYY-MM-DD format. |
| `nationalInsuranceNumber` | string | no | National insurance number. |
| `address1` | string | yes | Primary address line. |
| `address2` | string | yes | Secondary address line. |
| `county` | string | yes | County or state. |
| `phone` | string | yes | Phone number. |
| `postcode` | string | yes | Postal code. |
| `city` | string | yes | City. |
| `emergencyContactName` | string | yes | Emergency contact name. |
| `emergencyContactPhone` | string | yes | Emergency contact phone. |
| `emergencyContactRelationship` | string | yes | Emergency contact relationship. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "address2": "string",
      "city": "string",
      "county": "string",
      "dob": "string",
      "emergencyContactName": "Ava Chen",
      "emergencyContactPhone": "string",
      "emergencyContactRelationship": "string",
      "gender": "string",
      "id": 1,
      "nationalInsuranceNumber": "string",
      "phone": "string",
      "postcode": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `address2` | string |  |
| `city` | string |  |
| `county` | string |  |
| `dob` | string |  |
| `emergencyContactName` | string |  |
| `emergencyContactPhone` | string |  |
| `emergencyContactRelationship` | string |  |
| `gender` | string |  |
| `id` | number |  |
| `nationalInsuranceNumber` | string |  |
| `phone` | string |  |
| `postcode` | string |  |
| `title` | string |  |

## Native endpoint

Through the native RotaCloud API, this operation is `PATCH /v2/users/onboard/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-onboarding.md) for the provider-specific parameters and requirements.

