# Lasso X: Get Related People

Retrieves related people for a CVR entity from Lasso X.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-related-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-related-people?connectionId=$CONNECTION_ID&lasso_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lasso_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-related-people?${params}`, {
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
      "": [
        {
          "address": {
            "value": {
              "address1": "string",
              "postalCode": 1,
              "postalDistrict": "string"
            }
          },
          "board": [
            {
              "lassoId": "string"
            }
          ],
          "email": "ava@example.com",
          "firstName": "Ava",
          "lassoId": "string",
          "lastName": "Chen",
          "lastUpdated": "2026-05-07T12:00:00.000Z",
          "management": [
            {
              "lassoId": "string",
              "name": "Ava Chen",
              "role": {
                "type": "string"
              }
            }
          ],
          "name": "Ava Chen",
          "owner": [
            {
              "lassoId": "string",
              "ownership": {
                "from": 1
              }
            }
          ],
          "phone": "string",
          "type": "string",
          "unitNumber": 1
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
| `[].address.value.address1` | string |  |
| `[].address.value.postalCode` | number |  |
| `[].address.value.postalDistrict` | string |  |
| `[].board[].lassoId` | string |  |
| `[].email` | string |  |
| `[].firstName` | string |  |
| `[].lassoId` | string |  |
| `[].lastName` | string |  |
| `[].lastUpdated` | date |  |
| `[].management[].lassoId` | string |  |
| `[].management[].name` | string |  |
| `[].management[].role.type` | string |  |
| `[].name` | string |  |
| `[].owner[].lassoId` | string |  |
| `[].owner[].ownership.from` | number |  |
| `[].phone` | string |  |
| `[].type` | string |  |
| `[].unitNumber` | number |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /:lassoId/related/person` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-related-people.md) for the provider-specific parameters and requirements.

