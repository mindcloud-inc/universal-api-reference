# Harbour: List Agreement Link Submissions

Retrieves submissions for an agreement link from Harbour.

```
GET https://connect.mindcloud.co/v1/universal/harbour/latest/actions/list-agreement-link-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/list-agreement-link-submissions?connectionId=$CONNECTION_ID&agreement_link_id=ng3E2dsKK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agreement_link_id": "ng3E2dsKK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harbour/latest/actions/list-agreement-link-submissions?${params}`, {
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
| `agreement_link_id` | string | yes | Agreement link identifier whose submissions you want to list. Example: `ng3E2dsKK`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "pages": 1,
      "size": 1,
      "submissions": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number |  |
| `pages` | number |  |
| `size` | number |  |
| `submissions` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Harbour API, this operation is `GET https://api.harbourshare.com/v1/agreement_links/:agreement_link_id/submissions` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agreement-link-submissions.md) for the provider-specific parameters and requirements.

