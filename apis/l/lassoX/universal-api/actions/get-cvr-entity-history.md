# Lasso X: Get CVR Entity History

Retrieves CVR entity history from Lasso X by Lasso ID.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-cvr-entity-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-cvr-entity-history?connectionId=$CONNECTION_ID&lasso_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lasso_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-cvr-entity-history?${params}`, {
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
      "address": [
        {
          "value": {
            "address1": "string",
            "postalCode": 1
          }
        }
      ],
      "cvr": 1,
      "email": [
        {
          "value": "ava@example.com"
        }
      ],
      "form": [
        {
          "value": {
            "code": 1
          }
        }
      ],
      "industry": [
        {
          "value": {
            "text": "string"
          }
        }
      ],
      "lassoId": "string",
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "lifeTime": [
        {
          "value": {
            "from": "2026-05-07T12:00:00.000Z",
            "to": "2026-05-07T12:00:00.000Z"
          }
        }
      ],
      "name": [
        {
          "current": true,
          "from": "2026-05-07T12:00:00.000Z",
          "to": "2026-05-07T12:00:00.000Z",
          "value": "Ava Chen"
        }
      ],
      "phone": [
        {
          "value": "string"
        }
      ],
      "status": [
        {
          "current": true,
          "from": "2026-05-07T12:00:00.000Z",
          "value": "string"
        }
      ],
      "unitNumber": 1,
      "website": [
        {
          "value": "string"
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
| `address[].value.address1` | string |  |
| `address[].value.postalCode` | number |  |
| `cvr` | number |  |
| `email[].value` | string |  |
| `form[].value.code` | number |  |
| `industry[].value.text` | string |  |
| `lassoId` | string |  |
| `lastUpdated` | date |  |
| `lifeTime[].value.from` | date |  |
| `lifeTime[].value.to` | date |  |
| `name[].current` | boolean |  |
| `name[].from` | date |  |
| `name[].to` | date |  |
| `name[].value` | string |  |
| `phone[].value` | string |  |
| `status[].current` | boolean |  |
| `status[].from` | date |  |
| `status[].value` | string |  |
| `unitNumber` | number |  |
| `website[].value` | string |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /:lassoId/history` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cvr-entity-history.md) for the provider-specific parameters and requirements.

