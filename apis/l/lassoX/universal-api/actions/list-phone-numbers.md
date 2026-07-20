# Lasso X: List Phone Numbers

Retrieves phone numbers for a Lasso X entity.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-phone-numbers?connectionId=$CONNECTION_ID&lasso_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lasso_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-phone-numbers?${params}`, {
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
| `lasso_id` | string | yes | Lasso ID, for example CVR-1-34580820. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cvr": 1,
      "phoneNumbers": [
        {
          "added": "2026-05-07T12:00:00.000Z",
          "anonymousPrepaidIndicator": true,
          "cvr": 1,
          "movementDate": "2026-05-07T12:00:00.000Z",
          "pNumber": 1,
          "supplier": "string",
          "telephoneNumber": 1
        }
      ],
      "robinson": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cvr` | number |  |
| `phoneNumbers[].added` | date |  |
| `phoneNumbers[].anonymousPrepaidIndicator` | boolean |  |
| `phoneNumbers[].cvr` | number |  |
| `phoneNumbers[].movementDate` | date |  |
| `phoneNumbers[].pNumber` | number |  |
| `phoneNumbers[].supplier` | string |  |
| `phoneNumbers[].telephoneNumber` | number |  |
| `robinson` | boolean |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /data/teledata/:lassoId/phonenumbers` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-phone-numbers.md) for the provider-specific parameters and requirements.

