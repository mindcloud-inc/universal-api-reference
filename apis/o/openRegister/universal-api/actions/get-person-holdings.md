# OpenRegister: Get Person Holdings

Retrieves a person's holdings from OpenRegister.

```
GET https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-person-holdings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRegister `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-person-holdings?connectionId=$CONNECTION_ID&personId=person_id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "person_id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-person-holdings?${params}`, {
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
| `personId` | string | yes | Unique person identifier. Example: `person_id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "holdings": [
        {}
      ],
      "person_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `holdings` | array<object> | Person holdings. |
| `person_id` | string | Person ID. |

## Native endpoint

Through the native OpenRegister API, this operation is `GET /v1/person/:person_id/holdings` (base URL `https://api.openregister.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-holdings.md) for the provider-specific parameters and requirements.

