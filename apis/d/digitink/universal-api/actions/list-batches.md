# Digit.ink: List Batches



```
GET https://connect.mindcloud.co/v1/universal/digitink/latest/actions/list-batches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digit.ink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitink/latest/actions/list-batches?connectionId=$CONNECTION_ID&key=batchUuid&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "batchUuid",
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitink/latest/actions/list-batches?${params}`, {
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
| `key` | list | yes | Digit.ink batch filter key. One of: `batchUuid`, `credentialTitle`, `issued`, `ltiData`, `templateName`, `templateUuid`. |
| `value` | string | yes | Digit.ink batch filter value. |

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

Through the native Digit.ink API, this operation is `GET /batches` (base URL `https://app.digit.ink/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-batches.md) for the provider-specific parameters and requirements.

