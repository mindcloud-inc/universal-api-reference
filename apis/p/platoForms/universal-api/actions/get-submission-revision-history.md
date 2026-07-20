# PlatoForms: Get Submission Revision History

Retrieves submission revision history from PlatoForms.

```
GET https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-submission-revision-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-submission-revision-history?connectionId=$CONNECTION_ID&submission_identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submission_identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-submission-revision-history?${params}`, {
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
| `submission_identifier` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "histories": {},
      "id": "string",
      "total_revision": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `histories` | object |  |
| `id` | string |  |
| `total_revision` | number |  |

## Native endpoint

Through the native PlatoForms API, this operation is `GET /submission/rev/{{submission_identifier}}/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission-revision-history.md) for the provider-specific parameters and requirements.

