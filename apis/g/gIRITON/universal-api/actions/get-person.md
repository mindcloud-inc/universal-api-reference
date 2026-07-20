# GIRITON: Get Person

Retrieves a specific person from GIRITON.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-person?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-person?${params}`, {
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
| `id` | string | yes | Person ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "departments": [
        {}
      ],
      "email": "ava@example.com",
      "employmentEndDate": "string",
      "employmentStartDate": "string",
      "entryTimestamp": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "number": "string",
      "presenceCardIds": [
        "string"
      ],
      "tags": [
        "string"
      ],
      "weeklyWorkHourFund": 1,
      "weeklyWorkHourFundTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departments` | array<object> | Department assignments. |
| `email` | string | Work email address. |
| `employmentEndDate` | string | Employment end date as returned by GIRITON. |
| `employmentStartDate` | string | Employment start date as returned by GIRITON. |
| `entryTimestamp` | date | Person entry timestamp. |
| `firstName` | string | First name. |
| `id` | string | Person ID. |
| `lastName` | string | Last name. |
| `number` | string | Person number. |
| `presenceCardIds` | array<string> | Presence card IDs. |
| `tags` | array<string> | Person tags. |
| `weeklyWorkHourFund` | number | Weekly work hour fund. |
| `weeklyWorkHourFundTotal` | number | Total weekly work hour fund. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /hr/person/:id` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

