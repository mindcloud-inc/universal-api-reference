# Satori Cyber: Get Dataset Access Details

Retrieves dataset access details from Satori Cyber.

```
GET https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/get-dataset-access-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Satori Cyber `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/get-dataset-access-details?connectionId=$CONNECTION_ID&datasetId=ds_12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "ds_12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/get-dataset-access-details?${params}`, {
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
| `datasetId` | string | yes | Dataset identifier. Example: `ds_12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableAccessRules": [
        {}
      ],
      "description": "string",
      "id": "string",
      "instantAccessRule": {},
      "name": "Ava Chen",
      "pendingRequest": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableAccessRules` | array<object> |  |
| `description` | string |  |
| `id` | string |  |
| `instantAccessRule` | object |  |
| `name` | string |  |
| `pendingRequest` | object |  |

## Native endpoint

Through the native Satori Cyber API, this operation is `GET /api/v1/dataset/:datasetId/access-details` (base URL `https://app.satoricyber.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dataset-access-details.md) for the provider-specific parameters and requirements.

