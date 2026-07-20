# Harbour: Get Agreement Link Submission

Retrieves a specific agreement link submission from Harbour.

```
GET https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-agreement-link-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-agreement-link-submission?connectionId=$CONNECTION_ID&agreement_link_id=ng3E2dsKK&submission_id=AGREESUBMISSION-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agreement_link_id": "ng3E2dsKK",
  "submission_id": "AGREESUBMISSION-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-agreement-link-submission?${params}`, {
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
| `agreement_link_id` | string | yes | Agreement link identifier. Example: `ng3E2dsKK`. |
| `submission_id` | string | yes | Specific submission identifier. Example: `AGREESUBMISSION-123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "submission": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `submission` | object |  |

## Native endpoint

Through the native Harbour API, this operation is `GET https://api.harbourshare.com/v1/agreement_links/:agreement_link_id/submissions/:submission_id` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agreement-link-submission.md) for the provider-specific parameters and requirements.

