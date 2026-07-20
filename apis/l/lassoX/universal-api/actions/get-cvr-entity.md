# Lasso X: Get CVR Entity

Retrieves a CVR entity from Lasso X by Lasso ID.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-cvr-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-cvr-entity?connectionId=$CONNECTION_ID&lasso_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lasso_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-cvr-entity?${params}`, {
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
      "address": {
        "address1": "string",
        "postalCode": 1,
        "postalDistrict": "string"
      },
      "alternateNames": [
        "Ava Chen"
      ],
      "cvr": 1,
      "email": "ava@example.com",
      "employees": {
        "count": 1
      },
      "form": {
        "code": 1,
        "shortDescription": "string"
      },
      "industry": {
        "code": "string",
        "text": "string"
      },
      "lassoId": "string",
      "lastStatusChange": "2026-05-07T12:00:00.000Z",
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "lifeTime": {
        "from": "2026-05-07T12:00:00.000Z",
        "to": "2026-05-07T12:00:00.000Z"
      },
      "name": "Ava Chen",
      "phone": "string",
      "productionUnits": [
        {
          "lassoId": "string",
          "pNumber": 1
        }
      ],
      "purpose": "string",
      "status": "string",
      "unitNumber": 1,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.address1` | string |  |
| `address.postalCode` | number |  |
| `address.postalDistrict` | string |  |
| `alternateNames[]` | string |  |
| `cvr` | number |  |
| `email` | string |  |
| `employees.count` | number |  |
| `form.code` | number |  |
| `form.shortDescription` | string |  |
| `industry.code` | string |  |
| `industry.text` | string |  |
| `lassoId` | string |  |
| `lastStatusChange` | date |  |
| `lastUpdated` | date |  |
| `lifeTime.from` | date |  |
| `lifeTime.to` | date |  |
| `name` | string |  |
| `phone` | string |  |
| `productionUnits[].lassoId` | string |  |
| `productionUnits[].pNumber` | number |  |
| `purpose` | string |  |
| `status` | string |  |
| `unitNumber` | number |  |
| `website` | string |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /:lassoId` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cvr-entity.md) for the provider-specific parameters and requirements.

