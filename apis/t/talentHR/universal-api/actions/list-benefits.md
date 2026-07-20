# TalentHR: List Benefits

Retrieves benefits from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-benefits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-benefits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-benefits?${params}`, {
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
| `filter` | string | no | Optional TalentHR benefit filter ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "benefitCategory": {},
      "benefitCategoryId": 1,
      "benefitRequiredFor": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "requiredForAll": true,
      "startDate": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `benefitCategory` | object |  |
| `benefitCategoryId` | number |  |
| `benefitRequiredFor` | array<object> |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `description` | string |  |
| `endDate` | date |  |
| `id` | number |  |
| `name` | string |  |
| `requiredForAll` | boolean |  |
| `startDate` | date |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /benefits` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-benefits.md) for the provider-specific parameters and requirements.

