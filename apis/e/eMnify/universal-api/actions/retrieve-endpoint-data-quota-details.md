# EMnify: Retrieve Endpoint Data Quota Details

Retrieves endpoint data quota details from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/retrieve-endpoint-data-quota-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/retrieve-endpoint-data-quota-details?connectionId=$CONNECTION_ID&authToken=Paste%20the%20auth_token%20from%20Retrieve%20Authentication%20Token&endpointId=18811970" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authToken": "Paste the auth_token from Retrieve Authentication Token",
  "endpointId": "18811970"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/retrieve-endpoint-data-quota-details?${params}`, {
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
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. Example: `Paste the auth_token from Retrieve Authentication Token`. |
| `endpointId` | number | yes | Endpoint ID to inspect. Example: `18811970`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionOnExhaustion": {
        "description": "string",
        "id": 1
      },
      "autoRefill": 1,
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "lastStatusChangeDate": "2026-05-07T12:00:00.000Z",
      "lastVolumeAdded": 1,
      "peakThroughput": 1,
      "status": {
        "description": "string",
        "id": 1
      },
      "thresholdPercentage": 1,
      "thresholdVolume": 1,
      "volume": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionOnExhaustion.description` | string |  |
| `actionOnExhaustion.id` | number |  |
| `autoRefill` | number |  |
| `expiryDate` | date |  |
| `lastStatusChangeDate` | date |  |
| `lastVolumeAdded` | number |  |
| `peakThroughput` | number |  |
| `status.description` | string |  |
| `status.id` | number |  |
| `thresholdPercentage` | number |  |
| `thresholdVolume` | number |  |
| `volume` | number |  |

## Native endpoint

Through the native EMnify API, this operation is `GET /endpoint/:endpoint_id/quota/data` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-endpoint-data-quota-details.md) for the provider-specific parameters and requirements.

