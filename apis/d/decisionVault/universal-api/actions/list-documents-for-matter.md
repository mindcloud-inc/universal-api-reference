# DecisionVault: List Documents for Matter

Retrieves documents for a matter in DecisionVault.

```
GET https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-documents-for-matter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DecisionVault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-documents-for-matter?connectionId=$CONNECTION_ID&matterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "matterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-documents-for-matter?${params}`, {
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
| `matterId` | string | yes | The matter ID. |
| `uploadedSince` | date | no | Only include documents uploaded on or after this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_id": "string",
      "document_request": {},
      "download_url": "https://example.com",
      "expires_in": 1,
      "filename": "Ava Chen",
      "size": 1,
      "uploaded_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_id` | string |  |
| `document_request` | object |  |
| `download_url` | string |  |
| `expires_in` | number |  |
| `filename` | string |  |
| `size` | number |  |
| `uploaded_at` | date |  |

## Native endpoint

Through the native DecisionVault API, this operation is `GET /matters/:matter_id/documents` (base URL `https://api.decisionvault.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents-for-matter.md) for the provider-specific parameters and requirements.

