# Oboloo: Create Subindustry

Creates a new subindustry in Oboloo.

```
POST https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-subindustry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oboloo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-subindustry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "industries_id": "string",
  "sub_industry_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-subindustry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "industries_id": "string",
    "sub_industry_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `industries_id` | string | yes | Industry identifier that this subindustry belongs to. |
| `sub_industry_name` | string | yes | Name of the subindustry to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "id": 1,
      "industriesId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | number |  |
| `id` | number |  |
| `industriesId` | string |  |
| `updatedAt` | date |  |
| `value` | string |  |

## Native endpoint

Through the native Oboloo API, this operation is `POST /configuration/addsubIndustry` (base URL `https://mindcloudwizard20260330.oboloo.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subindustry.md) for the provider-specific parameters and requirements.

