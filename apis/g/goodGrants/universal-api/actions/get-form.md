# Good Grants: Get form

Retrieves a form from Good Grants.

```
GET https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Good Grants `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/get-form?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/get-form?${params}`, {
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
| `slug` | string | yes | Form slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callToAction": "string",
      "chapterOption": "string",
      "contentBlock": {},
      "created": "2026-05-07T12:00:00.000Z",
      "name": {},
      "season": {},
      "slug": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callToAction` | string |  |
| `chapterOption` | string |  |
| `contentBlock` | object |  |
| `created` | date |  |
| `name` | object |  |
| `season` | object |  |
| `slug` | string |  |
| `type` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Good Grants API, this operation is `GET form/:slug` (base URL `https://api.cr4ce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

