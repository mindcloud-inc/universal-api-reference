# Digit.ink: Get Batch



```
GET https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digit.ink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-batch?connectionId=$CONNECTION_ID&batchUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-batch?${params}`, {
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
| `batchUuid` | string | yes | Batch UUID path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchLength": 1,
      "batchUuid": "string",
      "chain": "string",
      "credentialTitle": "string",
      "credentialType": "string",
      "credentialVersion": "string",
      "hasPassword": true,
      "isArchived": true,
      "issued": "2026-05-07T12:00:00.000Z",
      "issuerUri": "string",
      "lmsData": {},
      "originalBatchLength": 1,
      "productKey": "string",
      "templateName": "Ava Chen",
      "templateUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchLength` | number |  |
| `batchUuid` | string |  |
| `chain` | string |  |
| `credentialTitle` | string |  |
| `credentialType` | string |  |
| `credentialVersion` | string |  |
| `hasPassword` | boolean |  |
| `isArchived` | boolean |  |
| `issued` | date |  |
| `issuerUri` | string |  |
| `lmsData` | object |  |
| `originalBatchLength` | number |  |
| `productKey` | string |  |
| `templateName` | string |  |
| `templateUuid` | string |  |

## Native endpoint

Through the native Digit.ink API, this operation is `GET /batches/:batchUuid` (base URL `https://app.digit.ink/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch.md) for the provider-specific parameters and requirements.

