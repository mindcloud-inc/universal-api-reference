# Digit.ink: Issue Credentials



```
POST https://connect.mindcloud.co/v1/universal/digitink/latest/actions/issue-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digit.ink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digitink/latest/actions/issue-credentials" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productKey": "BLOCKCHAIN_CREDENTIALS",
  "templateUuid": "string",
  "csvString": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitink/latest/actions/issue-credentials', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productKey": "BLOCKCHAIN_CREDENTIALS",
    "templateUuid": "string",
    "csvString": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productKey` | list | yes | Digit.ink product key. One of: `BLOCKCHAIN_CREDENTIALS`, `DIGITAL_CREDENTIALS`, `RECIPIENTS`. |
| `templateUuid` | string | yes | Template UUID for credential issuance. |
| `csvString` | string | yes | CSV string containing credential recipients. |
| `credentialTitle` | string | no | Optional credential title override. |
| `description` | string | no | Optional credential description override. |
| `lmsData` | string | no | Optional LMS data payload string. |
| `isTestRun` | boolean | no | Whether to run the issue request as a test. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchUuid": "string",
      "credentialUuids": [
        "string"
      ],
      "errors": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchUuid` | string |  |
| `credentialUuids` | array<string> |  |
| `errors` | array<object> |  |

## Native endpoint

Through the native Digit.ink API, this operation is `POST /credentials` (base URL `https://app.digit.ink/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/issue-credentials.md) for the provider-specific parameters and requirements.

