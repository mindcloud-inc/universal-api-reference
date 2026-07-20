# FillFaster: Create Submission Link

Creates a unique submission link in FillFaster.

```
POST https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/create-submission-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FillFaster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/create-submission-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/create-submission-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fid` | string | yes | Form template identifier. |
| `prefillData` | object | no | Field values to prefill into the generated submission link. |
| `userData` | object | no | Opaque metadata returned back in FillFaster webhooks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "submissionId": "string",
      "submissionLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `submissionId` | string | Created FillFaster submission identifier. |
| `submissionLink` | string | Generated FillFaster submission URL. |

## Native endpoint

Through the native FillFaster API, this operation is `POST /v1/createSubmission` (base URL `https://api.fillfaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-submission-link.md) for the provider-specific parameters and requirements.

