# Oboloo: Create Industry

Creates a new industry in Oboloo.

```
POST https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-industry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oboloo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-industry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "industry_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-industry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "industry_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `industry_name` | string | yes | Name of the industry to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "industry": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "createdBy": 1,
        "id": 1,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "value": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `industry.createdAt` | date |  |
| `industry.createdBy` | number |  |
| `industry.id` | number |  |
| `industry.updatedAt` | date |  |
| `industry.value` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Oboloo API, this operation is `POST /configuration/addIndustry` (base URL `https://mindcloudwizard20260330.oboloo.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-industry.md) for the provider-specific parameters and requirements.

