# Go4Clients: Create Shortlink Campaign

Creates a new shortlink campaign in Go4Clients.

```
POST https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-shortlink-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-shortlink-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud shortlink campaign",
  "programId": "5bb63583b5615f00085fb1a5",
  "expirationDays": "5",
  "input": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-shortlink-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud shortlink campaign",
    "programId": "5bb63583b5615f00085fb1a5",
    "expirationDays": "5",
    "input": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the shortlink campaign. Example: `MindCloud shortlink campaign`. |
| `programId` | string | yes | Program identifier the campaign belongs to. Example: `5bb63583b5615f00085fb1a5`. |
| `expirationDays` | number | yes | How many days the shortlink remains available. Example: `5`. |
| `description` | string | no | Optional shortlink campaign description. Example: `Shortlink campaign for MindCloud`. |
| `input` | object | yes | Shortlink input object with type and either baseUrl or landing details. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingProduct": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingProduct` | string | Billing product associated with the campaign. |
| `creationDate` | date | Campaign creation date. |
| `description` | string | Description of the shortlink campaign. |
| `expirationDate` | date | Campaign expiration date. |
| `id` | string | Identifier of the shortlink campaign. |
| `name` | string | Name of the shortlink campaign. |

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/campaigns/shortlink/v1.0` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shortlink-campaign.md) for the provider-specific parameters and requirements.

