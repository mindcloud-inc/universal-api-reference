# VoilaNorbert: Submit Bulk File

Submits a bulk email search file to VoilaNorbert.

```
POST https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/submit-bulk-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoilaNorbert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/submit-bulk-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/submit-bulk-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `colCompany` | string | no | CSV column index containing the company name. |
| `colName` | string | no | CSV column indexes containing first and last name values. |
| `content` | string | no | Raw CSV content to upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "created": 1,
      "enrich": true,
      "enrich_token": "string",
      "filename": "Ava Chen",
      "id": 1,
      "list_id": 1,
      "quantity": 1,
      "rerun_frequency": 1,
      "rerun_last_time": 1,
      "started": 1,
      "status": "string",
      "success": 1,
      "treated": 1,
      "updated": 1,
      "webhook": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `created` | number |  |
| `enrich` | boolean |  |
| `enrich_token` | string |  |
| `filename` | string |  |
| `id` | number |  |
| `list_id` | number |  |
| `quantity` | number |  |
| `rerun_frequency` | number |  |
| `rerun_last_time` | number |  |
| `started` | number |  |
| `status` | string |  |
| `success` | number |  |
| `treated` | number |  |
| `updated` | number |  |
| `webhook` | string |  |

## Native endpoint

Through the native VoilaNorbert API, this operation is `POST /massives/` (base URL `https://api.voilanorbert.com/2018-01-08`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-bulk-file.md) for the provider-specific parameters and requirements.

