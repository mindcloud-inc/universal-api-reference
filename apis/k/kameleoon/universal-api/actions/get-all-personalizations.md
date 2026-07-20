# Kameleoon: Get all personalizations



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-personalizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-personalizations?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-personalizations?${params}`, {
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
| `paramsIo` | string | yes | Required query object documented by Kameleoon for list endpoints. Example: `page=1, perPage=20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributionWindow": 1,
      "category": "string",
      "collectingDataEnabled": true,
      "createdBy": 1,
      "customExpositionRate": 1,
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateEnded": "2026-05-07T12:00:00.000Z",
      "dateModified": "2026-05-07T12:00:00.000Z",
      "dateStarted": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "format": "string",
      "goals": [
        1
      ],
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributionWindow` | number |  |
| `category` | string |  |
| `collectingDataEnabled` | boolean |  |
| `createdBy` | number |  |
| `customExpositionRate` | number |  |
| `dateCreated` | date |  |
| `dateEnded` | date |  |
| `dateModified` | date |  |
| `dateStarted` | date |  |
| `description` | string |  |
| `format` | string |  |
| `goals` | array<number> |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Kameleoon API, this operation is `GET personalizations` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-personalizations.md) for the provider-specific parameters and requirements.

