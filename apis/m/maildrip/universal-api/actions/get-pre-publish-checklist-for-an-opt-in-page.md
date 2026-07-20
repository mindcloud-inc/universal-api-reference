# Maildrip: Get pre-publish checklist for an opt-in page



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-pre-publish-checklist-for-an-opt-in-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-pre-publish-checklist-for-an-opt-in-page?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-pre-publish-checklist-for-an-opt-in-page?${params}`, {
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
| `pageId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `success` | boolean | Indicates whether the request was processed successfully. |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/opt-in-pages/{pageId}/pre-publish-check` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pre-publish-checklist-for-an-opt-in-page.md) for the provider-specific parameters and requirements.

