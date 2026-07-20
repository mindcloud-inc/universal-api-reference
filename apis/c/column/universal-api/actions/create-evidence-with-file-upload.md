# Column: Create Evidence With File Upload



```
POST https://connect.mindcloud.co/v1/universal/column/latest/actions/create-evidence-with-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/column/latest/actions/create-evidence-with-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityId": "string",
  "file": "string",
  "purpose": "Active Status Certificate",
  "documentType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/create-evidence-with-file-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityId": "string",
    "file": "string",
    "purpose": "Active Status Certificate",
    "documentType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityId` | string | yes |  |
| `file` | file | yes |  |
| `purpose` | list | yes | One of: `Active Status Certificate`, `Adverse Media Screening`, `Attestation Account Info Truth`, `Attestation Beneficial Ownership`, `Attestation Control Person`, `Attestation Privacy Policy`, `Attestation Terms of Service`, `Business Formation`, `Complete Customer File`, `EDD`, `IRS Form 990`, `IRS Form SS4`, `Identity Verification`, `Nonprofit Other Evidence`, `OFAC Screening`, `PEP Screening`, `Proof of Address`, `Signed Account Agreement`, `Tax ID Confirmation`. |
| `documentType` | string | yes |  |
| `description` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Column API returns.

## Native endpoint

Through the native Column API, this operation is `POST /entities/:entity_id/evidence` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-evidence-with-file-upload.md) for the provider-specific parameters and requirements.

